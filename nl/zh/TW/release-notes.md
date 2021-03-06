---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-07"

subcollection: personality-insights

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:deprecated: .deprecated}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# 版本注意事項
{: #release-notes}

下列各節記載 {{site.data.keyword.personalityinsightsshort}} 服務每一個版次所包括的新特性和變更。除非另有說明，否則所有變更皆與舊版相容，可自動透通地用於所有新的和現有的應用程式。
{: shortdesc}

此版本注意事項記載所有最新更新項目的*服務版本* 和*介面版本*。使用 `version` 查詢參數來指定*介面版本*，以使用該更新所提供的新增特性和功能。服務會以 `X-Service-Api-Version` 回應標頭來傳回這兩個版本。
{: note}

## 2018 年 12 月 21 日
{: #December2018}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

已從服務移除了 {{site.data.keyword.personalityinsightsshort}} API 的第 2 版。服務的第 3 版於 2016 年 10 月 19 日發行。當時已強烈建議使用者儘快從第 2 版進行移轉。

## 2018 年 11 月 18 日
{: #November2018b}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

{{site.data.keyword.personalityinsightsshort}} 服務現在可用於「{{site.data.keyword.cloud}} 倫敦」位置 (**eu-gb**)。與所有位置一樣，倫敦使用記號型 Identity and Access Management (IAM) 鑑別。您在這個位置建立的所有新服務實例都使用 IAM 鑑別。

## 2018 年 11 月 7 日
{: #November2018a}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

{{site.data.keyword.personalityinsightsshort}} 服務現在可用於「{{site.data.keyword.cloud_notm}} 東京」位置 (**jp-tok**)。與所有位置一樣，東京使用記號型 Identity and Access Management (IAM) 鑑別。您在這個位置建立的所有新服務實例都使用 IAM 鑑別。

## 舊版本
{: #older}

-   [2018 年 10 月 30 日](#October2018)
-   [2018 年 6 月 11 日](#June2018b)
-   [2018 年 6 月 4 日](#June2018a)
-   [2018 年 3 月 23 日](#March2018)
-   [2017 年 10 月 13 日](#October2017)
-   [2017 年 9 月 18 日](#September2017)
-   [2017 年 4 月 10 日](#April2017)
-   [2017 年 3 月 1 日](#March2017)
-   [2017 年 2 月 20 日](#February2017b)
-   [2017 年 2 月 13 日](#February2017)
-   [2017 年 1 月 13 日](#January2017)
-   [2016 年 12 月 15 日](#December2016)
-   [2016 年 11 月 15 日](#November2016)
-   [2016 年 10 月 20 日](#October2016b)
-   [2016 年 10 月 12 日](#October2016a)
-   [2016 年 8 月 31 日](#August2016)
-   [2016 年 7 月 14 日](#July2016b)
-   [2016 年 7 月 1 日](#July2016a)
-   [2016 年 6 月 7 日](#June2016b)
-   [2016 年 6 月 1 日](#June2016a)
-   [2016 年 5 月 17 日](#May2016)
-   [2016 年 3 月 18 日](#March2016)
-   [2015 年 7 月 9 日](#July2015)
-   [2015 年 2 月 23 日](#February2015)

### 2018 年 10 月 30 日
{: #October2018}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

{{site.data.keyword.personalityinsightsshort}} 服務已移轉至所有位置的記號型 Identity and Access Management (IAM) 鑑別。所有 {{site.data.keyword.cloud_notm}} 服務現在都使用 IAM 鑑別。{{site.data.keyword.personalityinsightsshort}} 服務會在下列日期時對每一個位置進行移轉：

-   達拉斯 (**us-south**)：2018 年 10 月 30 日
-   法蘭克福 (**eu-de**)：2018 年 10 月 30 日
-   華盛頓特區 (**us-east**)：2018 年 6 月 11 日
-   雪梨 (**au-syd**)：2018 年 6 月 4 日

移轉至 IAM 鑑別對新的和現有服務實例的影響不同：

-   *在任何位置中建立的所有新服務實例*現在都使用 IAM 鑑別來存取服務。您可以傳遞載送記號或 API 金鑰：記號支援未在每個呼叫中內嵌服務認證的已鑑別要求；API 金鑰會使用 HTTP 基本鑑別。當您使用任何 {{site.data.keyword.watson}} SDK 時，您可以傳遞 API 金鑰，並讓 SDK 管理記號的生命週期。
-   *在指出的移轉日期之前，您在某個位置中建立的現有服務實例*，會繼續使用先前於 Cloud Foundry 服務認證中的 `{username}` 及 `{password}` 以進行鑑別，直到您將它們更新為使用 IAM 鑑別。因為 {{site.data.keyword.personalityinsightsshort}} 服務為無狀態，您可以執行下列步驟將現有服務實例轉換為使用 IAM 鑑別：

    1.  刪除並重建服務實例。
    1.  修改應用程式碼以使用 IAM 鑑別。

如需相關資訊，請參閱下列文件：

-   如果要瞭解服務實例使用的鑑別機制，請按一下 [{{site.data.keyword.cloud_notm}} 儀表板 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/dashboard/apps){: new_window} 上的實例，來檢視您的服務認證。
-   如需搭配 Watson 服務來使用 IAM 記號的相關資訊，請參閱[使用 IAM 記號進行鑑別](/docs/services/watson?topic=watson-iam)。
-   如需搭配 Watson 服務來使用 IAM API 金鑰的相關資訊，請參閱 [IAM 服務 API 金鑰](/docs/services/watson?topic=watson-api-key-bp)。
-   如需使用 IAM 鑑別的範例，請參閱 [API 參考資料 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/personality-insights){: new_window}。

### 2018 年 6 月 11 日
{: #June2018b}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

對於在華盛頓特區（**us-east**）中管理的服務實例及應用程式，服務現在支援新的 API 鑑別處理程序。如需相關資訊，請參閱 [2018 年 10 月 30 日服務更新](#October2018)。

### 2018 年 6 月 4 日
{: #June2018a}

**服務版本** - `3.4.5`<br/> **介面版本** - `2017-10-13`

對於在雪梨（**au-syd**）中管理的服務實例及應用程式，服務現在支援新的 API 鑑別處理程序。如需相關資訊，請參閱 [2018 年 10 月 30 日服務更新](#October2018)。

### 2018 年 3 月 23
{: #March2018}

**服務版本** - `3.4.4`<br/> **介面版本** - `2017-10-13`

-   服務更新了小型問題修正程式。這些變更特定用於阿拉伯文、日文和韓文。
-   `Accept` 要求標頭現在需要搭配 `POST /v3/profile` 方法一起使用。您必須指定 `application/json` 或 `text/csv`。

### 2017 年 10 月 13 日
{: #October2017}

**服務版本** - `3.4.0`<br/> **介面版本** - `2017-10-13`

-   現在性格設定檔的 `Trait` 物件還包括 `significant` 欄位。對於每一個「五大性格特質」維度、「五大性格特質」面向、「需求」和「價值觀」，都會以個別的 `Trait` 物件來報告其結果。每一個物件實例的 `significant` 欄位都會識別該特質的結果對於要求的輸入語言 (`Content-Language`) 是否有意義。

    -   若為英文、西班牙文和日文，所有性格特質的這個欄位一律為 `true`。
    -   對於阿拉伯文和韓文的大部分性格特質，此欄位為 `true`，但對於其服務模型無法為其產生有意義的結果，則此欄位為 `false`。對於特質的常數集，此欄位為 `false`。如需完整清單，請參閱[阿拉伯文和韓文輸入的限制](/docs/services/personality-insights?topic=personality-insights-numeric#limitations)。請不要採信此欄位為 `false` 之任何特質的結果。

    如需服務之 JSON 回應內容的相關資訊，請參閱[瞭解 JSON 設定檔](/docs/services/personality-insights?topic=personality-insights-output)。
-   CSV 輸出現在還包括標題名稱為 `*_significant` 的直欄。每一個直欄都提供一個布林值，指出該特質是否有意義。如需服務之 CSV 回應內容的相關資訊，請參閱[瞭解 CSV 設定檔](/docs/services/personality-insights?topic=personality-insights-outputCSV)。
-   如果要使用這個最新版本的介面，請以 `version` 參數指定介面版本 `2017-10-13`。

### 2017 年 9 月 18 日
{: #September2017}

**服務版本** - `3.3.0`<br/> **介面版本** - `2016-10-19`

服務現在支援韓文 (`ko`) 的輸入內容。如需韓文輸入的平均「平均絕對誤差 (MAE)」和平均相關性的相關資訊，請參閱[每種語言的平均 MAE 和相關性](/docs/services/personality-insights?topic=personality-insights-science#precisePerLanguage)。

對於韓文輸入的幾項性格特質，服務的模型無法產生有意義的百分位數和原始評分。如需這些特質的結果相關資訊，請參閱[阿拉伯文和韓文輸入的限制](/docs/services/personality-insights?topic=personality-insights-numeric#limitations)。

### 2017 年 4 月 10 日
{: #April2017}

**服務版本** - `3.1.7`<br/> **介面版本** - `2016-10-19`

-   服務變更了處理含有大量輸入內容之要求的方式。服務最多可接受 20 MB 的內容。不過，對於以 *GloVe* 為依據的模型，精確度會在大約 3000 個輸入字詞開始趨於平穩。此行為與舊模型不同，在舊模型中，文字愈多，所產生的精確度愈高。一般而言，服務不再需要這麼多內容，即可產生精確的設定檔。但是，更多內容需要更多的處理時間，這會導致要求在完成之前逾時。

    因此，服務現在只會從大型的要求中擷取並使用前 250 KB 內容（任何 HTML 或 JSON 標記皆不計算在內）。此數字並未對映確切的字數，這會依文字的語言和本質而異。例如，英文的平均字詞長度介於四到五個字元之間，所以此數字提供大約 50,000 個字詞，比服務所需的字數至少高出 15 倍。回應 JSON 的 `word_count` 欄位會指出服務用於要求的字數，這會少於輸入中的字數。

    因為其作為設定檔依據的字數，還是比最高精確度絕對需要的字數多很多，所以服務產生的設定檔跟以前一樣精確。不過，服務回應的速度比以前快很多。對於只用到部分輸入內容的要求，服務會傳回下列 `CONTENT_TRUNCATED` 警告訊息，讓使用者知道這個事實：

    `For maximum accuracy while also optimizing processing time, only the first 250KB of input text (excluding markup) was analyzed. Accuracy levels off at approximately 3K words so this did not affect the accuracy of the profile.`

    如需相關資訊，請參閱[提供足夠的輸入](/docs/services/personality-insights?topic=personality-insights-input#sufficient)。
-   服務更新了小型安全修正程式。

### 2017 年 3 月 1
{: #March2017}

**服務版本** - `3.1.6`<br/> **介面版本** - `2016-10-19`

服務更新了小型記載的加強功能。

### 2017 年 2 月 20 日
{: #February2017b}

**服務版本** - `3.1.5.1`<br/> **介面版本** - `2016-10-19`

此服務更新了小型安全和問題修正程式，並改善 API 呼叫的計量。

### 2017 年 2 月 13 日
{: #February2017}

**服務版本** - `3.1.4`<br/> **介面版本** - `2016-10-19`

-   已精簡消費喜好清單。此清單現在只包括瞭解個人主要生活方式習慣和消費者特質所需的最重要項目。已將消費喜好清單從 51 縮短為 42。其餘的偏好更簡明扼要地表達作者喜好不同產品、服務及活動的可能性，以便更容易對結果採取行動。

    服務不再傳回下列九項消費喜好：

    -   <code>consumption_preferences_shopping</code> 種類不再包含
        -   <code>consumption_preferences_automobile_resale_value</code>
    -   <code>consumption_preferences_reading</code> 種類不再包含
        -   <code>consumption_preferences_read_motive_enjoyment</code><br/>
        -   <code>consumption_preferences_read_motive_information</code><br/>
        -   <code>consumption_preferences_read_motive_mandatory</code><br/>
        -   <code>consumption_preferences_read_motive_relaxation</code>
    -   <code>consumption_preferences_health_and_activity</code> 種類不再包含
        -   <code>consumption_preferences_adventurous_sports</code>
        -   <code>consumption_preferences_fast_food_frequency</code>
    -   <code>consumption_preferences_volunteering</code> 種類不再包含
        -   <code>consumption_preferences_volunteering_time</code>
        -   <code>consumption_preferences_volunteer_learning</code>

    如需其餘喜好的相關資訊，請參閱[消費喜好](/docs/services/personality-insights?topic=personality-insights-preferences)。
-   *若為阿拉伯文輸入*，現在可以在[每種語言的平均 MAE 和相關性](/docs/services/personality-insights?topic=personality-insights-science#precisePerLanguage)中找到平均「平均絕對誤差 (MAE)」和平均相關性的相關資訊。此外，對於部分性格特質，服務的模型無法產生有意義的百分位數和原始評分。如需這些特質的結果相關資訊，請參閱[阿拉伯文和韓文輸入的限制](/docs/services/personality-insights?topic=personality-insights-numeric#limitations)。

### 2017 年 1 月 13 日
{: #January2017}

**服務版本** - `3.1.2.1`<br/> **介面版本** - `2016-10-19`

Personality Insights 服務更新了幾項小型問題修正程式。

### 2016 年 12 月 15 日
{: #December2016}

**服務版本** - `3.1.1`<br/> **介面版本** - `2016-10-19`

若為阿拉伯文輸入文字，{{site.data.keyword.personalityinsightsshort}} 服務現在使用 *GloVe* 來開發性格設定檔。服務不再對任何語言使用「語言查詢和字詞計數 (LIWC)」心理語言學詞典。如需服務如何開發性格側寫的相關資訊，請參閱[推斷性格特質的方式](/docs/services/personality-insights?topic=personality-insights-science#researchInfer)。

### 2016 年 11 月 15 日
{: #November2016}

**服務版本** - `3.1.0`<br/> **介面版本** - `2016-10-19`

-   若為日文輸入文字，{{site.data.keyword.personalityinsightsshort}} 服務現在使用 *GloVe* 來開發性格設定檔。服務不再對日文輸入使用「語言查詢和字詞計數 (LIWC)」心理語言學詞典。如需相關資訊，請參閱[推斷性格特質的方式](/docs/services/personality-insights?topic=personality-insights-science#researchInfer)。
-   現在會以 `Accept-Language` 要求標頭指定的語言，使用本地化字串傳回 `ConsumptionPreferencesCategory` 和 `ConsumptionPreferences` 物件的 `name` 欄位。
-   更新項目包括幾個小型問題修正程式。

### 2016 年 10 月 20 日
{: #October2016b}

**服務版本** - `3.0.0`<br/> **介面版本** - `2016-10-19`

{{site.data.keyword.personalityinsightsshort}} 服務及其 API 有重大更新。API 從第 2 版增至第 3 版，並提供新的特性。此版本注意事項的其餘部分會詳細說明這些變更。

第 3 版與第 2 版不相容。建議您移轉至第 3 版，以充分運用新的特性和變更。移轉至第 3 版只需要更新並重新部署您的應用程式，即可將這些版本注意事項中說明的變更用於新版本。您不需要在 {{site.data.keyword.cloud_notm}} 中建立新的服務實例；您只需要呼叫 `v3` API。

即將從服務移除第 2 版 {{site.data.keyword.personalityinsightsshort}} API。強烈建議您盡快移轉至第 3 版。
{: note}

#### 第 3 版的相關資訊

此文件現在說明第 3 版的 {{site.data.keyword.personalityinsightsshort}} API。下列各節彙總新版本介面的變更：

-   如需呼叫 `/v3/profile` 方法的相關資訊，請參閱[要求設定檔](/docs/services/personality-insights?topic=personality-insights-input)。
-   如需 `/v3/profile` 方法回應的相關資訊，請參閱[瞭解 JSON 設定檔](/docs/services/personality-insights?topic=personality-insights-output)和[瞭解 CSV 設定檔](/docs/services/personality-insights?topic=personality-insights-outputCSV)。
-   如需第 3 版介面的相關資訊，請參閱 [API 參考資料 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/personality-insights){: new_window}。

#### <code>/v3/profile</code> 方法的參數變更

`/v3/profile` 方法的參數已變更：

-   API 現在提供一個名為 `consumption_preferences` 的選用查詢參數。此參數接受布林值，用於指出是否要隨結果傳回關於消費喜好的推斷資訊。依預設，該資訊不會包括在回應中。如需相關資訊，請參閱[新的消費喜好特性](#cp)。
-   API 現在包含必要的 `version` 查詢參數。此參數接受的字串會以 `YYYY-MM-DD` 格式的日期來識別所要求的 API 版本和回應格式；例如，指定 `2016-10-19` 代表 2016 年 10 月 19 日。此參數容許服務針對新版本來更新其 API 或回應格式，而不會岔斷現有的用戶端。第 3 版 API 的起始字串為 `2016-10-19`。

    您指定的日期不需要完全符合服務的版本。服務會使用不超過所提供日期的版本。如果您指定的日期早於第 3 版的發行日期，則服務會使用第 3 版的 API。如果您指定的日期是未來的日期，或是晚於最新版本，則服務會使用最新版本。
-   `include_raw` 查詢參數的名稱現在是 `raw_scores`。
-   `headers` 查詢參數的名稱現在是 `csv_headers`。

#### 新的消費喜好特性
{: #cp}

消費喜好特性可指出作者表現出不同消費傾向的趨勢。當您將 `consumption_preferences` 查詢參數搭配 `true` 值傳遞至 `/v3/profile` 方法時，服務會以 `Profile` 物件傳回額外的結果：

-   `consumption_preferences` 欄位會提供 `ConsumptionPreferencesCategory` 物件的陣列。
-   每一個 `ConsumptionPreferencesCategory` 物件皆包括下列欄位：
    -   `consumption_preference_category_id`：其中一個消費喜好種類的 ID
    -   `name`：使用者可看見的種類名稱。
    -   `consumption_preferences`：是 `ConsumptionPreferences` 物件的陣列，針對種類的個別喜好提供輸入文字推斷的結果
-   每一個 `ConsumptionPreferences` 物件皆包括下列欄位：
    -   `consumption_preference_id`：其中一個消費喜好的 ID。
    -   `name`：使用者可看見的消費喜好名稱。
    -   `score`：消費喜好的評分：

        -   `0.0` 指出不太可能
        -   `0.5` 指出中立
        -   `1.0` 指出可能

        部分喜好的評分是二進位，不容許中立值。評分是依據從輸入文字推斷之結果的喜好指示，而不是正規化的百分位數。

如需消費喜好的相關資訊，請參閱[消費喜好](/docs/services/personality-insights?topic=personality-insights-preferences)。

無論使用 `Accept-Language` 要求標頭所指定的語言為何，一律會以英文傳回這兩個消費喜好物件的 `name` 欄位。
{: note}

#### JSON 物件和欄位的變更

JSON 輸入和輸出物件及其欄位已簡化並闡明：

-   在可隨要求傳遞至 `/v3/profile` 方法的 JSON `ContentItem` 物件中，已移除下列欄位：
    -   `userid`
    -   `sourceid`
    -   `charset`（先前已淘汰）

    您可以將這些物件放在 JSON 要求的主體中，作為 `Content` 物件的 `contentItems` 陣列元素。
-   `/v3/profile` 方法傳回之 JSON `Profile` 物件的下列欄位已變更：
    -   已移除下列欄位：
        -   `id`
        -   `source`
    -   `tree` 欄位已移除，由四個新欄位取代：
        -   `personality` 代表「五大性格特質」。
        -   `needs` 代表「需求」特質。
        -   `values` 代表「價值觀」特質。
        -   `behavior` 代表關於星期幾和幾點的內容分佈狀況的時間結果。只會針對具有時間戳記的 JSON 輸入傳回此欄位。

        此變更有效地將結果在 JSON `Profile` 物件中向上移一層，以刪除遞迴層次。
    -   `processed_lang` 欄位的名稱現在是 `processed_language`。
-   `/v3/profile` 方法傳回之 JSON `Trait` 物件的下列欄位已重新命名：
    -   JSON `Trait` 物件的 `id` 欄位名稱現在是 `trait_id`。
    -   JSON `Trait` 物件的 `percentage` 欄位名稱現在是 `percentile`。
-   `/v3/profile` 方法傳回之 JSON `Trait` 物件的下列欄位已移除：
    -   `sampling_error`
    -   `raw_sampling_error`

    服務現在會報告符合其結果精準度的平均「平均絕對誤差 (MAE)」。如需不同輸入文字數量之 MAE 的相關資訊，請參閱[提供足夠的輸入](/docs/services/personality-insights?topic=personality-insights-input#sufficient)。
-   對於 `Profile` 物件的 `personality`、`needs` 和 `values` 欄位，仍會傳回 JSON `Trait` 物件。但是 `behavior` 欄位會傳回包含下列欄位的 JSON 物件 `Behavior` 陣列：
    -   `trait_id`
    -   `name`
    -   `category`
    -   `percentage`

    此外，行為資訊不再以值的樹狀結構傳回。輸出由列出所有時間特質（星期幾和幾點）的單一陣列組成。
-   `/v3/profile` 方法可傳回之 JSON `Warnings` 物件的 `id` 欄位名稱現在是 `warnings_id`。

#### JSON ID 的變更
{: #ids}

服務針對 `Trait` 和新 `Behavior` 物件的 `traviit_id`（早期為 `id`）欄位傳回的 JSON ID 已變更：

-   「五大性格特質」維度的 ID 現在是以字串 `big5_` 開頭。
-   「五大性格特質」面向的 ID 現在是以字串 `facet_` 開頭。
-   「需求」的 ID 現在是以字串 `need_` 開頭。
-   「價值觀」的 ID 現在是以字串 `value_` 開頭。
-   所有時間特質的 ID 現在是以字串 `behavior_` 開頭。
-   與幾點相關之時間特質的 ID 現在是使用四位數 24 小時制（例如，`behavior_0000`），而不是 12 小時制（例如，`0:00 am`）。
-   所有字元現在都是小寫。
-   空格和連字號現在是底線。

#### CSV 標頭的變更
{: #headers}

服務可以為 CSV 輸出傳回的選用直欄標頭已變更：

-   針對 JSON 輸出的 `trit_id` 說明的所有變更，也適用於 CSV 標頭。
-   「五大性格特質」維度的原始評分標頭現在是以字串 `big5_` 開頭。
-   「五大性格特質」面向的原始評分標頭現在是以字串 `facet_` 開頭。
-   「需求」的原始評分標頭現在是以字串 `need_` 開頭。
-   「價值觀」的原始評分標頭現在是以字串 `value_` 開頭。
-   已處理之語言直欄的標頭現在是 `processed_language`，而不是 `processed_lang`。
-   不再傳回 `user` 和 `source_id` 直欄。
-   所有字元現在都是小寫。
-   空格和連字號現在是底線。

#### <code>visualize</code> 方法的移除

服務的第 2 版 API 包括已淘汰的 `visualize` 方法，在舊版中會使用此方法將呼叫 `/v3/profile` 方法的結果視覺化。`visualize` 方法已從服務的 API 中移除。服務會繼續提供 JavaScript 檔案集合，可讓您將設定檔視覺化成圖形。如需相關資訊，請參閱[將設定檔視覺化](/docs/services/personality-insights?topic=personality-insights-overviewDevelopers#visualize)。

### 2016 年 10 月 12 日
{: #October2016a}

若為西班牙文輸入文字，{{site.data.keyword.personalityinsightsshort}} 服務現在使用 *GloVe* 來開發性格設定檔。服務不再對西班牙文輸入使用「語言查詢和字詞計數 (LIWC)」心理語言學詞典。從 8 月 31 日起，服務已開始為英文輸入文字使用新的模型。它計劃很快就會將新模型套用至其餘的輸入語言。如需新模型的相關資訊，請參閱[推斷性格特質的方式](/docs/services/personality-insights?topic=personality-insights-science#researchInfer)。

### 2016 年 8 月 31 日
{: #August2016}

服務現在使用 *GloVe* 來開發性格設定檔。*GloVe*是一種開放程式碼字詞內嵌技術。如需相關資訊，請參閱[推斷性格特質的方式](/docs/services/personality-insights?topic=personality-insights-science#researchInfer)。服務僅針對英文輸入文字使用新的方法。對於其他語言，服務繼續使用「語言查詢和字詞計數 (LIWC)」心理語言學詞典。此服務計劃未來將會為所有語言使用開放式詞彙方法。

對於用於英文輸入的新模型，服務會為其訓練模型報告結果的平均「平均絕對誤差 (MAE)」。如需 MAE 如何隨不同輸入文字數量而變更的相關資訊，請參閱[提供足夠的輸入](/docs/services/personality-insights?topic=personality-insights-input#sufficient)。

{{site.data.keyword.IBM_notm}} 計劃未來將報告非英文模型的 MAE。{{site.data.keyword.IBM_notm}} 計劃使用 MAE 而非錯誤取樣，以根據您提供的輸入文字數量來判斷服務變更的精準度為何。

### 2016 年 7 月 14 日
{: #July2016b}

-   若為阿拉伯文輸入，服務現在可以基於效能的理由，刪減輸入文字的數量。在特定的臨界值，阿拉伯文結果的精確度並不會隨著更多字詞而提升。如果服務刪減阿拉伯文輸入文字，將會以下列訊息傳回 `PARTIAL_TEXT_USED` 警告：

    `The text provided to compute the profile was trimmed for performance reasons. This action does not affect the accuracy of the output, as not all of the input text was required.`
-   更新項目包括問題修正程式和內部改良。

### 2016 年 7 月 1 日
{: #July2016a}

-   服務的定價方案現在為 {{site.data.keyword.personalityinsightsshort}} 使用者提供更低的價格。如需相關資訊，請參閱 [{{site.data.keyword.cloud_notm}} 型錄 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/catalog/services/personality-insights/){: new_window} 中的 {{site.data.keyword.personalityinsightsshort}} 服務。
-   您可以使用 `Accept-Language` 標頭來指定的受支援回應語言清單，現在包括
    -   `ar`（阿拉伯文）
    -   `de`（德文）
    -   `en`（英文，預設值）
    -   `es`（西班牙文）
    -   `fr`（法文）
    -   `it`（義大利文）
    -   `ja`（日文）
    -   `ko`（韓文）
    -   `pt-br`（巴西葡萄牙文）
    -   `zh-cn`（簡體中文）
    -   `zh-tw`（繁體中文）

    如需相關資訊，請參閱[指定要求和回應語言](/docs/services/personality-insights?topic=personality-insights-input#languages-input)。
-   `/v2/profile` 方法現在可以傳回下列 HTTP 狀態碼：
    -   429 *太多要求*：服務為內容語言處理的要求太多。請稍候再重試要求。如果您針對該語言提交許多要求，請考慮對提交要求的速率進行節流控制。
    -   504 *閘道逾時*：要求逾時或花費太長的時間來處理。請稍候再重試要求。如果輸入包含太多字詞（例如，超過 20,000 個），請考慮減少字數，但仍維持有意義輸入的準則。

    該方法不再傳回 503 *服務無法使用*。如需可能回應碼的相關資訊，請參閱 [API 參考資料 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/personality-insights){: new_window}。
-   更新項目包括問題修正程式和內部改良。

### 2016 年 6 月 7 日
{: #June2016b}

-   服務現在支援「跨原點資源共用 (CORS)」，可容許瀏覽器型用戶端直接呼叫服務。如需相關資訊，請參閱 [CORS 支援](/docs/services/personality-insights?topic=personality-insights-overviewDevelopers#CORS)。
-   服務針對日文文字的效能已大幅提升。
-   更新項目包括問題修正程式和內部改良。

### 2016 年 6 月 1 日
{: #June2016a}

服務已針對問題修正程式和內部改良進行更新。新的最上層欄位 `warnings` 也會新增至服務所傳回的 JSON 結果。如需相關資訊，請參閱 [API 參考資料 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/personality-insights){: new_window}。

### 2016 年 5 月 17 日
{: #May2016}

服務已針對問題修正程式和內部改良進行更新。

### 2016 年 3 月 18 日
{: #March2016}

服務現在支援下列語言：

-   服務支援的輸入文字有四種語言：阿拉伯文 (`ar`)、英文 (`en`)、西班牙文 (`es`) 和日文 (`ja`)。若要指定語言，請為純文字和 HTML 輸入使用 HTTP `Content-Language` 標頭，或為 JSON 輸入使用 `ContentItem` 物件的 `language` 內容。
-   服務同樣支援這四種語言的回應。若要指定回應的語言，請使用 `Accept-Language` 標頭。

您可以將任何組合的語言用於輸入和回應。如果您未指示語言，則服務會預設為英文。如需相關資訊，請參閱[指定要求和回應語言](/docs/services/personality-insights?topic=personality-insights-input#languages-input)。您還可以參閱部落格文章 [{{site.data.keyword.IBM_notm}} {{site.data.keyword.watson}} {{site.data.keyword.personalityinsightsshort}} 現在已有阿拉伯文及日文支援 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/blogs/watson/2016/04/arabic-japanese-support-now-available-ibm-watson-personality-insights/){: new_window}。

因為需要比其他語言多非常多的計算週期來進行分析，所以阿拉伯文內容需要明顯較長的時間來處理。雖然服務對所有語言皆支援相同 20 MB 的輸入文字數量限制，但是阿拉伯文內容的實際限制可能會較低，以避免逾時。日文內容也需要較長的時間來處理，但延遲的重要性較阿拉伯文低。
{: note}

### 2015 年 7 月 9 日
{: #July2015}

-   *語言支援。*您可以分析英文和西班牙文內容。您可以使用 `/v2/profile` 方法的 `Content-Language` 標頭來指出輸入文字的語言。如需指定語言的相關資訊，請參閱[指定要求和回應語言](/docs/services/personality-insights?topic=personality-insights-input#languages-input)。
-   *原始評分。*您可以要求從輸入文字和服務模型計算的原始評分和原始取樣誤差。這些值不會正規化或與樣本母體比較。針對想要為特定實務範例套用自訂正規化，或是不需要與樣本母體進行比較的客戶，原始評分非常有用。您可以將 `/v2/profile` 方法的 `include_raw` 查詢參數設為 `true`，以要求原始評分。如需相關資訊，請參閱[解譯數值結果](/docs/services/personality-insights?topic=personality-insights-numeric)。
-   *模型加強功能。*根據其最新的研究，{{site.data.keyword.IBM_notm}} 進一步改良一些推斷性格特質的方法。這些變更對服務的使用者是透明可見的；它們不會使先前從服務取得的任何結果失效。如需這些研究和服務推斷方式的相關資訊，請參閱[推斷性格特質的方式](/docs/services/personality-insights?topic=personality-insights-science#researchInfer)。

### 2015 年 2 月 23 日
{: #February2015}

從 2015 年 2 月 23 日開始，{{site.data.keyword.personalityinsightsshort}} 服務為先前 User Modeling 服務的一般可用 (GA) 版本，之前是以測試版提供。GA 版本需要使用者移轉至新服務的實例。服務的測試版與 GA 版本之間有下列差異存在。

-   {{site.data.keyword.personalityinsightsshort}} 服務與 User Modeling 服務相容。所說明的差異可提供更多的彈性和改良的結果，而不會影響現行應用程式。
-   您在 {{site.data.keyword.cloud_notm}} 中用來建立服務的參數已變更。您現在使用的服務名稱為 `personality_insights`，而非 `user_modeling`，服務方案為 `"IBM Watson Personality Insights Monthly Plan"`，而非 `user_modeling_free_plan`。
-   `/v2/profile` 方法接受兩個新的輸入格式。`Content-Type` 標頭現在接受的輸入格式，除了 JSON (`application/json`) 之外，還有純文字 (`text/plain`)（預設值）和 HTML (`text/html`)。
-   `/v2/profile` 方法現在會傳回新的輸出格式。`Accept` 標頭現在接受的輸出格式，除了 JSON (`application/json`)（預設值）之外，還有 CSV (`text/csv`)。
-   對於會為其報告百分比值的每一個特質，`/v2/profile` 方法現在會包括新的輸出元素 `sampling_error`。取樣誤差會以倍精準數值傳回，以指出服務根據輸入文字，對作者百分位數的信任度。
-   「需求」模型會採用改良的記號化和處理程序，以將其特質的值分佈進行更好的正規化。建議您重新計算 User Modeling API 所產生的任何結果。
-   `visualize` 方法現在已淘汰，並且會在未來版本中整個移除。您可以使用範例應用程式隨附的 `personality.js` JavaScript 檔案，從用戶端達到類似的結果。`textsummary.js` JavaScript 檔為服務的結果提供額外的格式。
