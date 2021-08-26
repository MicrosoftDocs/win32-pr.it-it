---
description: Interlacciamento video
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Interlacciamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474337"
---
# <a name="video-interlacing"></a>Interlacciamento video

Questo argomento descrive come le origini multimediali e i decodificatori devono gestire il contenuto video interlacciato.

Per decodificare ed eseguire correttamente il rendering del video interlacciato, sono necessarie le informazioni seguenti:

-   Progressivo o interlacciato. Un flusso video può contenere fotogrammi progressivi, fotogrammi interlacciati o una combinazione di entrambi.

-   Dominanza dei campi. La dominanza dei campi descrive il campo visualizzato per primo, il campo superiore o il campo inferiore.

-   Ripetere il primo campo. Questo flag viene usato nel pulldown 3:2, quando il frame è progressivo ma il flusso è interlacciato. In questo contesto, il primo campo può essere il campo superiore o inferiore.

-   Campi interleaved o campo singolo. Un esempio può contenere un singolo campo o due campi interfoliati. Se un campione contiene un singolo campo, l'altezza del campione è metà dell'altezza del frame, perché il campione contiene solo la metà delle righe di analisi per un frame. I campi interfoliati sono consigliati a meno che le caratteristiche del contenuto di origine non impongono il contrario.

Una qualsiasi di queste caratteristiche può cambiare da un campione a quello successivo. Tuttavia, i componenti video devono conoscere il contenuto complessivo prima dell'inizio dello streaming. Ad esempio, se il video è interlacciato, il renderer video avanzato (EVR) deve riservare memoria video per la deinterlacing. Se invece il video è interamente progressivo, l'EVR può ottimizzare la pipeline di rendering. L'aggiunta di un passaggio di deinterlacing alla pipeline aumenta la latenza di rendering.

Le informazioni sull'interlacciamento vengono archiviate in due posizioni:

-   Le informazioni generali sull'interlacciamento in un flusso vengono inserite nel tipo di supporto. Per altre informazioni sui tipi di supporti, vedere [Tipi di supporti](media-types.md).

-   Le informazioni che possono cambiare con ogni esempio vengono inserite nell'esempio come attributo. Per altre informazioni sugli esempi, vedere [Esempi multimediali](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Informazioni interlacciate nel tipo di supporto

[**L'attributo \_ MF MT \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md) nel tipo di supporto descrive come viene interlacciato il flusso nel suo complesso. Il valore di questo attributo è un membro [**dell'enumerazione MFVideoInterlaceMode.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) Un tipo di supporto video deve sempre avere questo attributo.

-   Se il flusso contiene solo fotogrammi progressivi, senza fotogrammi interlacciati, usare MFVideoInterlace \_ Progressive.
-   Se il flusso contiene solo fotogrammi interlacciati e ogni esempio contiene due campi interleaved, usare MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Se il flusso contiene solo fotogrammi interlacciati e ogni esempio contiene un singolo campo, usare MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower. Se i campi si alternano tra superiore e inferiore, non è importante quale di questi due valori viene usato. Se il formato contiene solo campi superiori o solo campi inferiori, impostare il valore corrispondente al contenuto.
-   Se il flusso contiene una combinazione di fotogrammi interlacciati e progressivi o se la dominanza del campo cambia, impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive. Usare attributi di esempio per descrivere ogni frame.

Nella tabella seguente viene riepilogato questo attributo.



| MODALITÀ \_ INTERLACE MF MT \_ \_                       | Interlacciato? | Esempi                                  | Primo campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ Progressivo                 | No          | Frame progressivo                        | Non applicabile |
| Campo \_ MFVideoInterlaceInterleavedUpperFirst  | Sì         | Campi interfoliati                       | Prima in alto    |
| Campo \_ MFVideoInterlaceInterleavedLowerFirst  | Sì         | Campi interfoliati                       | Prima in basso    |
| MFVideoInterlace \_ FieldSingleUpper            | Sì         | Campo singolo                             | Prima in alto    |
| MFVideoInterlace \_ FieldSingleLower            | Sì         | Campo singolo                             | Prima in basso    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Può variare    | Campi interfoliati o fotogrammi progressivi | Può variare       |



 

I campi interleaved e i singoli campi non possono essere misti. Il passaggio da uno a un altro richiede una modifica del tipo di supporto.

## <a name="interlace-flags-on-samples"></a>Flag interlacciati sugli esempi

Le informazioni che possono cambiare da un campione a quello successivo vengono indicate usando attributi di esempio. Usare [**l'interfaccia IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per ottenere o impostare questi attributi.

Tutti gli attributi di interlacciamento elencati in questa sezione hanno valori booleani. In effetti, ognuno di questi attributi può avere tre valori: **TRUE,** **FALSE** o non impostato. Se un attributo non è impostato, il valore viene derivato dal tipo di supporto. Se un attributo è impostato, il valore esegue l'override del tipo di supporto. Alcune combinazioni di flag e tipi di supporti non sono valide.




| Attributo | Descrizione | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | Se <strong>TRUE,</strong>il frame è interlacciato. Se <strong>FALSE,</strong>il frame è progressivo.<br /> Impostare questo attributo su ogni esempio se il tipo di supporto è MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | Il significato di questo flag dipende dal fatto che gli esempi contengano campi interleaved o singoli campi.<br /><ul><li>Campi interfoliati: se <strong>TRUE,</strong>il campo inferiore è il primo. Se <strong>FALSE,</strong>il campo superiore è il primo.<br /></li><li>Campi singoli: se <strong>TRUE,</strong>l'esempio contiene un campo inferiore. Se <strong>FALSE,</strong>l'esempio contiene un campo superiore.<br /></li></ul>Impostare questo attributo su ogni esempio di interlacciato se il tipo di supporto è MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | Se <strong>TRUE,</strong>il primo campo viene ripetuto. Se <strong>FALSE</strong> o non è impostato, il primo campo non viene ripetuto. | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | Se <strong>TRUE,</strong>l'esempio contiene un singolo campo. Se <strong>FALSE,</strong>l'esempio contiene campi interleaved. | 




 

La tabella seguente mostra quali flag sono obbligatori, facoltativi o non consentiti, in base al tipo di supporto.



| Tipo supporto         | Flag interlacciato                      | BottomFieldFirst Flag                    | RepeatFirstField Flag | SingleField Flag                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| Progressivo        | Facoltativo. se impostato, deve essere **FALSE.** | Non impostare.                              | Non impostare.           | Non impostare.                          |
| Campi interleaved | Facoltativo. se impostato, deve essere **TRUE.**  | Facoltativo. se impostato, deve corrispondere al tipo di supporto. | Non impostare.           | Facoltativo. se impostato, deve essere **FALSE.** |
| Campi singoli      | Facoltativo. se impostato, deve essere **TRUE.**  | Obbligatorio.                                | Non impostare.           | Impostare su **TRUE.**                     |
| Mixed              | Obbligatorio.                            | Obbligatorio.                                | Obbligatorio.             | Facoltativo. se impostato, deve essere **FALSE.** |



 

Nei casi in cui l'attributo è facoltativo, il tipo di supporto definisce già le informazioni. È possibile impostare l'attributo in modo che corrisponda, ma non è obbligatorio.

Ad esempio, se il tipo di supporto è MFVideoInterlace Progressive, significa che tutti i \_ fotogrammi nel flusso sono progressivi. Pertanto, è possibile impostare **l'attributo \_ interlacciato MFSampleExtension** su **FALSE** o lasciare l'attributo non impostato.

## <a name="recommendations"></a>Consigli

Questa sezione contiene raccomandazioni per vari tipi di contenuto.

1. Il video è tutti fotogrammi progressivi.

-   Impostare il tipo di supporto su MFVideoInterlace \_ Progressive.

-   Non impostare **l'attributo \_ interlacciato MFSampleExtension** o impostarlo su **FALSE** in ogni frame.

-   Non impostare gli attributi **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField.**

2. Il video è tutti campi interlacciati con la stessa dominanza dei campi. Gli esempi contengono campi interleaved.

-   Impostare il tipo di supporto su MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   Non impostare **l'attributo \_ interlacciato MFSampleExtension** o impostarlo su **TRUE** in ogni frame.

-   Non impostare **l'attributo MFSampleExtension \_ BottomFieldFirst** o impostare il valore in ogni frame in modo che corrisponda al tipo di supporto.

-   Non impostare **l'attributo MFSampleExtension \_ RepeatFirstField** o impostarlo su **FALSE** in ogni frame.

-   Non impostare **l'attributo \_ SingleField MFSampleExtension** o impostarlo su **FALSE** in ogni frame.

3. Il video contiene una combinazione di fotogrammi interlacciati e progressivi, con campi ripetuti e dominanza del campo variabile (ad esempio, video DVD).

-   Impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   In ogni frame impostare gli attributi **MFSampleExtension \_ Interlaced**, **MFSampleExtension \_ BottomFieldFirst** e **MFSampleExtension \_ RepeatFirstField.**

-   Non impostare **l'attributo \_ SingleField MFSampleExtension** o impostarlo su **FALSE** in ogni frame.

4. Il video è interlacciato e gli esempi contengono campi singoli.

-   Impostare il tipo di supporto su MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.

-   In ogni frame impostare **l'attributo MFSampleExtension \_ BottomFieldFirst.**

-   Non impostare **l'attributo \_ interlacciato MFSampleExtension** o impostarlo su **TRUE** in ogni frame.

-   Non impostare **l'attributo MFSampleExtension \_ RepeatFirstField** o impostarlo su **FALSE** in ogni frame.

-   Non impostare **l'attributo \_ SingleField MFSampleExtension** o impostarlo su **TRUE** in ogni frame.

La maggior parte del contenuto video rientra in una di queste categorie.

## <a name="mpeg-2-mappings"></a>Mapping MPEG-2

Per il contenuto MPEG-2, usare i mapping seguenti per convertire i flag MPEG-2 in Media Foundation di esempio.

**struttura \_ dell'immagine**



| valore         | Attributo di esempio                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **FALSE**                                                                          |
| campo \_ superiore    | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**<br/> |
| campo \_ inferiore | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**<br/>  |



 

**fotogramma \_ progressivo**



| valore | Attributo di esempio                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ INTERLACCIATO**  =  **TRUE**  |
| 1     | **MFSampleExtension \_ FALSE interlacciato**  =   |



 

**primo \_ campo \_ superiore**



| valore | Attributo di esempio                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE** |



 

**ripeti \_ il primo \_ campo**



| valore | Attributo di esempio                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **FALSE** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE**  |



 

## <a name="single-field-samples"></a>Single-Field esempi

Se il tipo di supporto è MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace FieldSingleLower, significa che ogni esempio contiene \_ un singolo campo. Tuttavia, il tipo di supporto descrive l'intero frame. Pertanto, ogni buffer contiene solo la metà del numero di righe di campo specificato nel tipo di supporto. Ad esempio, se il tipo di supporto descrive il video come 720 × 480, ogni campo contiene 240 righe di analisi e pertanto ogni buffer contiene solo 240 righe di pixel. Se si scrive un componente che accetta tipi di supporti con esempi a campo singolo, è necessario prendere in considerazione questo fatto quando si accede ai dati nel buffer.

La stessa regola si applica all'apertura geometrica[(attributo MF \_ MT GEOMETRIC \_ \_ APERTURE)](mf-mt-geometric-aperture-attribute.md) e all'apertura minima dello schermo[(attributo MF \_ MT MINIMUM DISPLAY \_ \_ \_ APERTURE).](mf-mt-minimum-display-aperture-attribute.md) Queste aree vengono specificate in termini dell'intero frame, non dei singoli campi.

## <a name="directshow-mappings"></a>DirectShow Mapping

In DirectShow, le informazioni di interlacciamento per campione sono contenute nel **membro dwTypeSpecificFlags** della **struttura AM \_ SAMPLE2 \_** PROPERTIES. Nella tabella seguente vengono illustrati gli attributi equivalenti per Media Foundation.



| DirectShow flag di esempio              | Media Foundation attributo di esempio                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ VIDEO \_ FLAG \_ INTERLEAVED \_ FRAME | **MFSampleExtension \_ SingleField**  =  **FALSE**.                                                                                                                                    |
| AM \_ VIDEO \_ FLAG \_ FIELD1             | **MFSampleExtension \_ Interlacciato**  =  **TRUE.**<br/> **MFSampleExtension \_ SingleField**  =  **TRUE.**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.**<br/> |
| AM \_ VIDEO \_ FLAG \_ FIELD2             | **MFSampleExtension \_ Interlacciato**  =  **TRUE.**<br/> **MFSampleExtension \_ SingleField**  =  **TRUE.**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE.**<br/>  |
| AM \_ VIDEO \_ FLAG \_ TESSITURA              | **MFSampleExtension \_ INTERLACCIATO**  =  **FALSE**. Questo flag indica che il driver non deve denterlacere i due campi.                                                        |
| AM \_ VIDEO \_ FLAG \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.** Se il contenuto è interlacciato e il \_ flag AM VIDEO FLAG \_ \_ FIELD1FIRST non è presente, impostare questo attributo su **TRUE.**        |
| CAMPO \_ DI RIPETIZIONE DEL FLAG VIDEO \_ \_ \_ AM      | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE.** Se il flag AM \_ VIDEO FLAG REPEAT FIELD non è \_ \_ \_ presente, impostare questo attributo su **FALSE.**                                    |



 

Se l DirectShow di esempio non contiene flag di esempio, usare il valore **di dwInterlaceFlags** dalla struttura **VIDEOINFOHEADER2:**



| DirectShow flag interlacciato    | Media Foundation di esempio                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_ Interlacciato**  =  **TRUE.**        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **TRUE.**       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.** |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 




