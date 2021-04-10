---
title: Effetto Mappa tono bianco
description: Questo effetto consente la scalabilità lineare del livello bianco di un'immagine. Questa operazione è particolarmente utile quando si esegue la conversione tra lo spazio luminanza a cui viene fatto riferimento e lo spazio di luminanza a cui viene fatto riferimento, o viceversa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 70a38f37f5a5461b968099bebe4be120a727c053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964458"
---
# <a name="white-level-adjustment-effect"></a>Effetto di regolazione del livello bianco

Questo effetto consente la scalabilità lineare del livello bianco di un'immagine. Questa operazione è particolarmente utile quando si esegue la conversione tra lo spazio luminanza a cui viene fatto riferimento e lo spazio di luminanza a cui viene fatto riferimento, o viceversa.

Le proprietà di questo effetto sono identificate dall' [**enumerazione D2D1_WHITELEVELADJUSTMENT_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)e il CLSID è **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Proprietà effetto

| Nome visualizzato e enumerazione dell'indice | Tipo e valore predefinito | Descrizione |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | Livello bianco dell'immagine di input, in nit. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | Livello bianco dell'immagine di output, in nit. |

## <a name="remarks"></a>Commenti
Questo effetto è concepito per essere combinato con l' [effetto Mappa dei toni HDR](hdr-tone-map-effect.md) per consentire di eseguire il rendering delle immagini HDR in Direct2D con la gestione dei colori e il mapping dei toni appropriati. Per ulteriori informazioni, vedere la **sezione Osservazioni** dell'argomento. Gli effetti sono mirati a qualsiasi Framework che desideri offrire una migliore esperienza di visualizzazione delle immagini HDR che gestisce tutti i formati di immagine HDR di Windows e si adatta alle funzionalità dello schermo, sia HDR che WCG/SDR.

In Windows, si presuppone che tutti i contenuti SDR/WCG si trovino in uno spazio di luminanza a cui viene fatto riferimento, vale a dire che il livello bianco del contenuto deve essere scalato fino al livello bianco dello schermo prima che venga presentato in finale. Tuttavia, non è sempre responsabilità dell'applicazione eseguire questa operazione. Al contrario, si presuppone che il contenuto HDR si trovi in uno spazio di luminanza a cui viene fatto riferimento in una scena, vale a dire che non deve essere ridimensionato in modo da corrispondere al livello bianco della visualizzazione. Ciò premesso, l'applicazione potrebbe avere la necessità di eseguire il ridimensionamento in alcune circostanze durante il rendering del contenuto HDR per assicurarsi che questo sia il risultato netto.

Quando il desktop di Windows è in modalità SDR o WCG, il desktop è composto in uno spazio di luminanza a cui viene fatto riferimento. Tuttavia, se il desktop di Windows è in modalità HDR, la composizione del desktop viene eseguita nello spazio di luminanza a cui viene fatto riferimento nella scena. Ciò premesso, il Gestione finestre desktop (DWM) esegue le regolazioni della luminanza (spesso denominate SDRBoost) per le superfici di composizione a 8 bit e che semplifica l'applicazione per questo caso. Il boost automatico significa anche che il ruolo dell'applicazione nella conversione da uno spazio di luminanza a un altro dipende dal formato di composizione usato dall'applicazione per presentare il contenuto.

Nella tabella seguente vengono descritti i casi in cui l'applicazione deve e non deve eseguire la regolazione del livello bianco, oltre a quanto dovrebbe essere la regolazione. In generale, la regolazione dipende da tre fattori.

1. Spazio cromatico contenuto input. Indica se il contenuto di input contiene o meno valori di luminanza HDR (High Dynamic Range). Il contenuto di WCG si comporta allo stesso modo di SDR per il comportamento della luminanza.
2. Formato di composizione. Il formato pixel della superficie di destinazione presentata allo DWM &mdash; , ad esempio una [catena di scambio](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) o una superficie di [composizione](/uwp/api/Windows.UI.Composition.ICompositionSurface). Quando si esegue il rendering tramite Direct2D, il valore è **Uint8** o **FP16**.
3. Modalità colore avanzata desktop. Se DWM viene eseguito in modalità SDR, WCG o HDR per la visualizzazione corrente. Ottenere queste informazioni tramite [**DXGI_OUTPUT_DESC1::**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) [**AdvancedColorInfo. CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

In base a questi tre fattori, è necessario impostare i valori appropriati per `InputWhiteLevel` le `OutputWhiteLevel` proprietà e.

|Contenuto di input|Formato composizione|Modalità colore avanzata|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Qualsiasi|N/D|N/D|
|SDR/WCG|**FP16**|SDR/WCG|N/D|N/D|
|SDR/WCG|**FP16**|HDR|SDRWhite|80|
|HDR|Qualsiasi|SDR/WCG|80|[**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|HDR|**UINT8**|HDR|80|SDRWhite|
|HDR|**FP16**|HDR|N/D|N/D|

Nella tabella, il valore 80 è il livello bianco di riferimento, in nit, per il contenuto sRGB o scRGB. A tale proposito, è possibile usare la costante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), definita in `d2d1effects_2.h` . Il valore `SDRWhite` è il numero di nit che la visualizzazione deve usare per visualizzare il contenuto sRGB bianco. È possibile recuperare questo valore accedendo alla proprietà [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) . Il valore N/A significa che la regolazione del livello bianco non viene utilizzata in questo scenario. è possibile rimuovere l'effetto dal grafico o impostare i valori per un no-op.

Si noti che, nei casi in cui non è necessaria alcuna modifica a livello di bianco da parte dell'applicazione, DWM o la visualizzazione potrebbe gestire la conversione dallo spazio di luminanza a cui viene fatto riferimento nella scena.

- In modalità SDR/WCG la conversione viene eseguita dopo la composizione di DWM e si applica a tutto il contenuto presentato a tale visualizzazione. Questa conversione viene eseguita in modo implicito nella visualizzazione.
- In modalità HDR la conversione viene eseguita automaticamente da DWM prima della composizione, purché la superficie di composizione dell'applicazione sia SDR.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 10, versione 1809 (10,0; Build 17763) app \[ Desktop \| UWP app\] |
| Intestazione | d2d1effects \_ 2. h |
| Libreria | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumerazione D2D1_WHITELEVELADJUSTMENT_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
