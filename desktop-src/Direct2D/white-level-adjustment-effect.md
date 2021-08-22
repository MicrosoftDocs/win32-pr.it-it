---
title: Effetto mappa tono bianco
description: Questo effetto consente di ridimensionare in modo lineare il livello bianco di un'immagine. Ciò è particolarmente utile quando si esegue la conversione tra lo spazio di luminance indicato dalla visualizzazione e lo spazio di luminance con riferimento alla scena o viceversa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 646ad47ad671618f29d1691878de93b5e5141855787c53fdad44025487835ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292631"
---
# <a name="white-level-adjustment-effect"></a>Effetto di regolazione del livello bianco

Questo effetto consente di ridimensionare in modo lineare il livello bianco di un'immagine. Ciò è particolarmente utile quando si esegue la conversione tra lo spazio di luminance indicato dalla visualizzazione e lo spazio di luminance con riferimento alla scena o viceversa.

Le proprietà per questo effetto sono identificate [**dall'enumerazione D2D1_WHITELEVELADJUSTMENT_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)e il CLSID è **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Proprietà degli effetti

| Enumerazione del nome visualizzato e dell'indice | Tipo e valore predefinito | Descrizione |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | Livello bianco dell'immagine di input, in nits. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | Livello bianco dell'immagine di output, in nits. |

## <a name="remarks"></a>Commenti
Questo effetto deve essere combinato con l'effetto mappa tono HDR per consentire il rendering delle immagini [HDR](hdr-tone-map-effect.md) in Direct2D con la corretta gestione del colore e il mapping dei toni. Per altri dettagli, **vedere la sezione Osservazioni** dell'argomento. Gli effetti sono destinati a qualsiasi framework che voglia offrire un'esperienza di visualizzazione delle immagini HDR ottimale che gestisca tutti i formati di immagine HDR di Windows e si adatti alle funzionalità dello schermo(hdr o WCG/SDR).

In Windows, si presuppone che tutto il contenuto SDR/WCG si trova in uno spazio di luminenza indicato dalla visualizzazione, vale a dire che il livello bianco del contenuto deve essere ridimensionato fino al livello bianco dello schermo prima che venga presentato. Tuttavia, non è sempre responsabilità dell'applicazione eseguire questa operazione. Al contrario, si presuppone che il contenuto HDR si trova in uno spazio di luminance con riferimento alla scena, vale a dire che non deve essere ridimensionato in modo che corrisponda al livello bianco dello schermo. Ciò detto, l'applicazione potrebbe dover eseguire il ridimensionamento in alcune circostanze durante il rendering del contenuto HDR per garantire che si tratta del risultato netto.

Quando il desktop Windows desktop è in modalità SDR o WCG, il desktop è composto in uno spazio di luminance indicato dal display. Tuttavia, se Windows desktop è in modalità HDR, la composizione del desktop avviene nello spazio di luminance indicato dalla scena. Detto questo, il Gestione finestre desktop (DWM) esegue regolazioni della luminance (spesso denominate SDRBoost) per le superfici di composizione a 8 bit e questo semplifica l'applicazione per questo caso. Anche in questo caso, la boost automatica significa che il ruolo dell'applicazione nella conversione da uno spazio di luminance a un altro dipende dal formato di composizione che l'applicazione usa per presentare il contenuto.

La tabella seguente descrive i casi in cui l'applicazione deve e non deve eseguire una regolazione del livello bianco, nonché il tipo di regolazione. In generale, la regolazione dipende da tre fattori.

1. Spazio colore del contenuto di input. Se il contenuto di input contiene valori di luminance HDR (High Dynamic Range) o meno. Il contenuto WCG si comporta allo stesso modo della SDR per il comportamento di luminance.
2. Formato di composizione. Formato pixel della superficie di destinazione presentata al DWM, ad esempio, una catena di scambio &mdash; o una superficie di [composizione.](/uwp/api/Windows.UI.Composition.ICompositionSurface) [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Quando si esegue il rendering con Direct2D, si tratta di **UINT8** o **FP16.**
3. Modalità colore avanzata del desktop. Indica se DWM è in esecuzione in modalità SDR, WCG o HDR per la visualizzazione corrente. Ottenere queste informazioni [**tramite DXGI_OUTPUT_DESC1::ColorSpace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) o [**AdvancedColorInfo.CurrentAdvancedColorKind.**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind)

In base a questi tre fattori, è necessario impostare i valori appropriati per le `InputWhiteLevel` proprietà `OutputWhiteLevel` e .

|Contenuto di input|Formato composizione|Modalità colore avanzata|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Qualsiasi|N/D|N/D|
|SDR/WCG|**FP16**|SDR/WCG|N/D|N/D|
|SDR/WCG|**FP16**|Hdr|SDRWhite|80|
|Hdr|Qualsiasi|SDR/WCG|80|[**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|Hdr|**UINT8**|Hdr|80|SDRWhite|
|Hdr|**FP16**|Hdr|N/D|N/D|

Nella tabella il valore 80 è il livello bianco di riferimento, in nits, per il contenuto sRGB o scRGB. A tale scopo, è possibile usare [**la D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), definita in `d2d1effects_2.h` . Il valore `SDRWhite` è il numero di nits che lo schermo deve usare per visualizzare il contenuto sRGB bianco. È possibile recuperare questo valore accedendo [**alla proprietà AdvancedColorInfo.SdrWhiteLevelInNits.**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) Il valore N/D indica che la regolazione del livello bianco non viene usata in questo scenario. È possibile rimuovere l'effetto dal grafico o impostare i valori per un'operazione no-op.

Si noti che, nei casi in cui non è necessaria una regolazione del livello bianco da parte dell'applicazione, il DWM o lo schermo potrebbe gestire la conversione dallo spazio di luminance indicato dallo schermo allo spazio di luminance con riferimento alla scena.

- In modalità SDR/WCG la conversione avviene dopo la composizione DWM e si applica a tutto il contenuto presentato a tale visualizzazione. La visualizzazione esegue in modo implicito questa conversione.
- In modalità HDR, la conversione viene eseguita automaticamente dal DWM prima della composizione, purché la superficie di composizione dell'applicazione sia SDR.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 10, versione 1809 (10.0; Build 17763) \[ app desktop \| UWP\] |
| Intestazione | d2d1effects \_ 2.h |
| Libreria | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_WHITELEVELADJUSTMENT_PROP enumerazione](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
