---
description: Interlacciamento video
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Interlacciamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308976"
---
# <a name="video-interlacing"></a>Interlacciamento video

Questo argomento descrive come le origini e i decodificatori multimediali devono gestire il contenuto video interlacciato.

Per decodificare e visualizzare correttamente il video interlacciato, sono necessarie le informazioni seguenti:

-   Progressivo o interlacciato. Un flusso video può contenere frame progressivi, frame interlacciati o una combinazione di entrambi.

-   Dominanza del campo. La dominanza dei campi descrive il campo che viene visualizzato per primo, il campo superiore o il campo inferiore.

-   Ripetere il primo campo. Questo flag viene usato nel riquadro a discesa 3:2, quando il frame è progressivo, ma il flusso è interlacciato. In questo contesto, il primo campo può essere il campo superiore o inferiore.

-   Campi con interfoliazione o campo singolo. Un esempio può essere costituito da un singolo campo o da due campi con interfoliazione. Se un esempio contiene un solo campo, l'altezza del campione è metà dell'altezza del fotogramma, perché l'esempio contiene solo metà delle righe di analisi per un frame. I campi con interfoliazione sono consigliati, a meno che le caratteristiche del contenuto di origine non impongano in altro modo.

Ognuna di queste caratteristiche può variare da un campione a quello successivo. Tuttavia, i componenti video devono conoscere il contenuto complessivo prima che lo streaming venga avviato. Se ad esempio il video è interlacciato, il renderer video avanzato (EVR) deve riservare memoria video per il deinterlacciamento. Se il video è costituito da frame completamente progressivi, invece, il EVR può ottimizzare la pipeline di rendering. L'aggiunta di un passaggio di deinterlacciamento alla pipeline comporta un aumento della latenza di rendering.

Le informazioni sul interlacciamento sono archiviate in due posizioni:

-   Le informazioni generali sull'interlacciamento in un flusso vengono inserite nel tipo di supporto. Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md).

-   Le informazioni che possono essere modificate con ciascun campione vengono inserite nell'esempio come attributo. Per ulteriori informazioni sugli esempi, vedere [esempi di supporti](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Informazioni interlacciate nel tipo di supporto

L' [**attributo \_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md) sul tipo di supporto descrive il modo in cui il flusso nel suo complesso è interlacciato. Il valore di questo attributo è un membro dell'enumerazione [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) . Un tipo di supporto video deve sempre avere questo attributo.

-   Se il flusso contiene solo frame progressivi, senza frame interlacciati, usare MFVideoInterlace \_ progressive.
-   Se il flusso contiene solo frame interlacciati e ogni esempio contiene due campi con interfoliazione, usare MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Se il flusso contiene solo frame interlacciati e ogni esempio contiene un solo campo, usare MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower. Se i campi si alternano tra maiuscole e minuscole, non è importante quale di questi due valori venga usato. Se il formato contiene solo campi superiori o solo i campi inferiore, impostare il valore corrispondente al contenuto.
-   Se il flusso contiene una combinazione di frame interlacciati e progressivi o se il valore di dominanza del campo cambia, impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive. Usare gli attributi di esempio per descrivere ogni frame.

Nella tabella seguente viene riepilogato questo attributo.



| \_modalità di \_ intreccio MF mt \_                       | Interlacciate? | Esempi                                  | Primo campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ progressive                 | No          | Frame progressivo                        | Non applicabile |
| \_FieldInterleavedUpperFirst MFVideoInterlace  | Sì         | Campi con interfoliazione                       | Primo piano    |
| \_FieldInterleavedLowerFirst MFVideoInterlace  | Sì         | Campi con interfoliazione                       | Inferiore prima    |
| \_FieldSingleUpper MFVideoInterlace            | Sì         | Campo singolo                             | Primo piano    |
| \_FieldSingleLower MFVideoInterlace            | Sì         | Campo singolo                             | Inferiore prima    |
| \_MixedInterlaceOrProgressive MFVideoInterlace | Può variare    | Campi con interfoliazione o frame progressivi | Può variare       |



 

I campi con interfoliazione e i campi singoli non possono essere misti. Per passare da una a un'altra è necessario modificare il tipo di supporto.

## <a name="interlace-flags-on-samples"></a>Flag interlacciamento negli esempi

Le informazioni che possono cambiare da un campione a quello successivo vengono indicate usando gli attributi di esempio. Usare l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per ottenere o impostare questi attributi.

Tutti gli attributi di interlacciamento elencati in questa sezione hanno valori booleani. In effetti, ognuno di questi attributi può avere tre valori: **true**, **false** o not set. Se un attributo non è impostato, il valore viene ricavato dal tipo di supporto. Se viene impostato un attributo, il valore esegue l'override del tipo di supporto. Alcune combinazioni di flag e tipi di supporto non sono valide.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></td>
<td>Se <strong>true</strong>, il frame è interlacciato. Se <strong>false</strong>, il frame è progressivo.<br/> Impostare questo attributo su ogni campione se il tipo di supporto è MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></td>
<td>Il significato di questo flag dipende dal fatto che gli esempi contengano campi con interfoliazione o singoli campi.<br/>
<ul>
<li>Campi con interfoliazione: se <strong>true</strong>, il campo inferiore è primo. Se <strong>false</strong>, il campo superiore è primo.<br/></li>
<li>Campi singoli: se <strong>true</strong>, l'esempio contiene un campo inferiore. Se <strong>false</strong>, l'esempio contiene un campo superiore.<br/></li>
</ul>
Impostare questo attributo su ogni esempio di interpolazione se il tipo di supporto è MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></td>
<td>Se <strong>true</strong>, il primo campo viene ripetuto. Se <strong>false</strong> o non è impostato, il primo campo non viene ripetuto.</td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></td>
<td>Se <strong>true</strong>, l'esempio contiene un solo campo. Se <strong>false</strong>, l'esempio contiene campi con interfoliazione.</td>
</tr>
</tbody>
</table>



 

La tabella seguente mostra quali flag sono obbligatori, facoltativi o non consentiti in base al tipo di supporto.



| Tipo supporto         | Flag interlacciato                      | Flag BottomFieldFirst                    | Flag RepeatFirstField | Flag SingleField                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| Progressivo        | Opzionale Se impostato, deve essere **false**. | Non impostare.                              | Non impostare.           | Non impostare.                          |
| Campi con interfoliazione | Opzionale Se impostato, deve essere **true**.  | Opzionale Se impostato, deve corrispondere al tipo di supporto. | Non impostare.           | Opzionale Se impostato, deve essere **false**. |
| Campi singoli      | Opzionale Se impostato, deve essere **true**.  | Obbligatorio.                                | Non impostare.           | Impostare su **true**.                     |
| Mixed              | Obbligatorio.                            | Obbligatorio.                                | Obbligatorio.             | Opzionale Se impostato, deve essere **false**. |



 

Nei casi in cui l'attributo è facoltativo, il tipo di supporto definisce già le informazioni. È valido impostare l'attributo in modo che corrisponda, ma non obbligatorio.

Se, ad esempio, il tipo di supporto è MFVideoInterlace \_ progressive, significa che tutti i frame nel flusso sono progressivi. Pertanto, è possibile impostare l'attributo **MFSampleExtension \_ interlacciato** su **false** o lasciare l'attributo non impostato.

## <a name="recommendations"></a>Consigli

Questa sezione contiene consigli per diversi tipi di contenuto.

1. Il video è di tutti i frame progressivi.

-   Impostare il tipo di supporto su MFVideoInterlace \_ progressive.

-   Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **false** in ogni frame.

-   Non impostare gli attributi **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField** .

2. Il video è tutti i campi interlacciati con la stessa dominanza del campo. Gli esempi contengono campi con interfoliazione.

-   Impostare il tipo di supporto su MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **true** in ogni frame.

-   Non impostare l'attributo **MFSampleExtension \_ BottomFieldFirst** o impostare il valore su ogni frame in modo che corrisponda al tipo di supporto.

-   Non impostare l'attributo **MFSampleExtension \_ RepeatFirstField** o impostarlo su **false** in ogni frame.

-   Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **false** in ogni frame.

3. Il video contiene una combinazione di frame interlacciati e progressivi, con campi ripetuti e dominanza del campo variabile (ad esempio, video DVD).

-   Impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   In ogni frame impostare gli attributi **MFSampleExtension \_ Interlaced**, **MFSampleExtension \_ BottomFieldFirst** e **MFSampleExtension \_ RepeatFirstField** .

-   Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **false** in ogni frame.

4. Il video è interlacciato e gli esempi contengono singoli campi.

-   Impostare il tipo di supporto su MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.

-   Impostare l'attributo **MFSampleExtension \_ BottomFieldFirst** in ogni frame.

-   Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **true** in ogni frame.

-   Non impostare l'attributo **MFSampleExtension \_ RepeatFirstField** o impostarlo su **false** in ogni frame.

-   Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **true** in ogni frame.

La maggior parte del contenuto video rientra in una di queste categorie.

## <a name="mpeg-2-mappings"></a>Mapping MPEG-2

Per il contenuto MPEG-2, usare i mapping seguenti per convertire i flag MPEG-2 in Media Foundation gli attributi di esempio.

**\_struttura immagine**



| Valore         | Attributo di esempio                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **false**                                                                          |
| \_campo superiore    | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**<br/> |
| \_campo inferiore | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**<br/>  |



 

**frame progressivo \_**



| Valore | Attributo di esempio                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ Interlacciato**  =  **true**  |
| 1     | **MFSampleExtension \_ Interlacciato**  =  **false** |



 

**\_primo campo \_ principale**



| Valore | Attributo di esempio                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **true**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **false** |



 

**Ripeti \_ primo \_ campo**



| Valore | Attributo di esempio                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **false** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **true**  |



 

## <a name="single-field-samples"></a>Esempi di Single-Field

Se il tipo di supporto è MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower, significa che ogni esempio contiene un solo campo. Tuttavia, il tipo di supporto descrive l'intero frame. Pertanto, ogni buffer contiene solo metà del numero di righe di campo specificate nel tipo di supporto. Ad esempio, se il tipo di supporto descrive il video come 720 × 480, ogni campo contiene 240 righe di analisi e quindi ogni buffer contiene solo 240 righe di pixel. Se si scrive un componente che accetta i tipi di supporto con esempi di campo singolo, è necessario tenere presente questo fatto quando si accede ai dati nel buffer.

La stessa regola si applica all'apertura geometrica (attributo di[ \_ \_ \_ apertura geometrica MF mt](mf-mt-geometric-aperture-attribute.md) ) e all'apertura di visualizzazione minima (attributo di[ \_ \_ \_ \_ apertura minima dello schermo MF mt](mf-mt-minimum-display-aperture-attribute.md) ). Queste aree vengono specificate in termini di intero frame, non dei singoli campi.

## <a name="directshow-mappings"></a>Mapping DirectShow

In DirectShow, le informazioni di interlacciamento per campione sono contenute nel membro **dwTypeSpecificFlags** della struttura delle **\_ \_ Proprietà SAMPLE2** . Nella tabella seguente vengono illustrati gli attributi equivalenti per Media Foundation.



| Flag di esempio DirectShow              | Media Foundation attributo di esempio                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cornice del flag video am con \_ \_ interfoliazione \_ | **MFSampleExtension \_ SingleField**  =  **false**.                                                                                                                                    |
| \_Flag video \_ am \_ Field1             | **MFSampleExtension \_ Interlacciato**  =  **true**.<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**.<br/> |
| \_Flag video \_ am \_ Field2             | **MFSampleExtension \_ Interlacciato**  =  **true**.<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**.<br/>  |
| \_trama del \_ flag \_ video am              | **MFSampleExtension \_ Interlacciato**  =  **false**. Questo flag indica che il driver non deve deinterlacciare i due campi.                                                        |
| \_Flag video \_ am \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. Se il contenuto è interlacciato e il flag \_ FIELD1FIRST del flag video am \_ \_ non è presente, impostare questo attributo su **true**.        |
| \_campo di \_ ripetizione del flag video \_ am \_      | **MFSampleExtension \_ RepeatFirstField**  =  **true**. Se il \_ \_ \_ flag di campo di ripetizione del contrassegno del video am \_ non è presente, impostare questo attributo su **false**.                                    |



 

Se l'esempio DirectShow non contiene flag di esempio, usare il valore di **dwInterlaceFlags** dalla struttura **VIDEOINFOHEADER2** :



| Flag interlacciamento DirectShow    | Media Foundation attributo di esempio                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ interlacciato    | **MFSampleExtension \_ Interlacciato**  =  **true**.        |
| \_1FIELDPERSAMPLE AMINTERLACE | **MFSampleExtension \_ SingleField**  =  **true**.       |
| \_FIELD1FIRST AMINTERLACE     | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 




