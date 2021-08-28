---
title: A Deinterlace Video
description: A Deinterlace Video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, video con risoluzione deinterlaced
- Windows Media Format SDK, telefono inverso
- Windows Media Format SDK, tele tele tele
- Advanced Systems Format (ASF), video deinterlaced
- ASF (Advanced Systems Format),video deinterlaced
- Advanced Systems Format (ASF), telefono inverso
- ASF (Advanced Systems Format), telefono inverso
- Advanced Systems Format (ASF), televideo
- ASF (Advanced Systems Format),televideo
- Video deinterlaced
- televideo inverso, informazioni
- telecina, about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef1d1a6fcee3bf43d2fb4451d4ef129e595471e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475767"
---
# <a name="to-deinterlace-video"></a>A Deinterlace Video

Alcune origini di video, ad esempio le schede di acquisizione video, forniscono dati video per la visualizzazione interlacciata. Ogni fotogramma del video interlacciato è costituito da due campi. Il campo superiore contiene la prima riga di video e ogni altra riga successiva. Il campo inferiore contiene la seconda riga di video e ogni altra riga successiva. Un campo contiene quindi tutte le righe pari e l'altro contiene tutte le righe dispari. I campi che costituiscono un frame rappresentano orari di presentazione leggermente diversi in modo che, se interleaved, non formino un'immagine statica.

Quando si vuole visualizzare video su un monitor del computer, ogni fotogramma del video deve essere visualizzato come un'unica immagine (questo metodo di visualizzazione del video un intero fotogramma alla volta è detto *video* progressivo). Se si visualizzano video interlacciati in modo progressivo, i fotogrammi potrebbero non apparire a destra, a causa della differenza di tempo tra i due campi. Il codec Windows Media Video e il codec Windows Media Video Advanced Profile supportano entrambi una funzionalità di pre-elaborazione che converte il contenuto interlacciato in fotogrammi progressivi.

Per ottenere il video di input deinterlace del codec, chiamare il [**metodo IWMWriterAdvanced2::SetInputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) L'impostazione da usare è \_ g wszDeinterlaceMode. Impostare la modalità di dinterlacing su uno dei valori seguenti.




| valore | Descrizione | 
|-------|-------------|
| WM_DM_NOTINTERLACED | L'input è progressivo. Usare questa impostazione per arrestare la deinterlacing quando in precedenza è stata impostata la modalità di deinterlacing su un altro valore. | 
| WM_DM_DEINTERLACE_NORMAL | Selezionare questa modalità per unire i campi pari e dispari di un frame interlacciato (usando un meccanismo di compensazione del movimento). Benefici:<br /><ul><li>Gli artefatti interlacciati dello schermo progressivo sono notevolmente ridotti.</li><li>Il codec Windows Media Video produce video compressi di qualità superiore.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZE | Selezionare questa modalità quando la risoluzione di output è dime o inferiore rispetto alla risoluzione di input. Ad esempio, usare questa modalità quando la risoluzione video di input è 640 x 480 pixel e la risoluzione video di output è 320 x 240 pixel. Benefici:<br /><ul><li>Gli artefatti interlacciati dello schermo progressivo sono notevolmente ridotti.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE | Selezionare questa modalità quando la risoluzione di output è dime o inferiore alla risoluzione di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore. Ad esempio, usare questa modalità quando la risoluzione video di input è di 640 x 480 pixel a 30 fotogrammi interlacciati/sec e la risoluzione video di output è di 320 x 240 pixel a 60 fotogrammi/sec. Benefici:<br /><ul><li>Ciò produce fotogrammi progressivi di alta qualità, perché ogni campo viene convertito in un frame e quindi non è necessario unire alcuna informazione.</li><li>Viene acquisito il movimento completo dei campi interlacciati.</li></ul> | 
| WM_DM_DEINTERLACE_INVERSETELECINE | Selezionare questa modalità per convertire video di 30 fotogrammi/sec teletrasmessi nei 24 fotogrammi/sec del film originale. Benefici:<br /><ul><li>La qualità della compressione migliora in modo significativo perché è necessario codificare solo 24 fotogrammi/sec anziché 30 fotogrammi/sec.</li><li>Poiché il risultato è progressivo, vengono realizzati gli stessi vantaggi di compressione e visualizzazione della deinterlacciatura.</li></ul> | 
| WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE | Selezionare questa modalità quando la risoluzione di output verticale è dime o inferiore rispetto alla risoluzione verticale di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore. Ad esempio, la risoluzione video verticale di input è di 640 x 480 pixel a 30 fotogrammi interlacciati/sec e la risoluzione video verticale di output è di 320 x 240 pixel a 60 fotogrammi/sec. Benefici:<br /><ul><li>Ciò produce fotogrammi progressivi di alta qualità, perché ogni campo viene convertito in un frame e quindi non è necessario unire alcuna informazione.</li><li>Viene acquisito il movimento completo dei campi interlacciati.</li></ul> | 




 

Per il contenuto misto, impostare la modalità di distribuzione in base alle esigenze prima di passare esempi di un nuovo tipo. Ad esempio, per avviare la codifica con l'input progressivo, non è necessario impostare alcuna modalità di dinterlacing. Se alcuni esempi richiedono una deinterlacciamento normale, è necessario impostare la modalità di deinterlacing su WM \_ DM \_ DEINTERLACE \_ NORMAL. Per elaborare altri campioni progressivi, è necessario impostare la modalità di deinterlacing su WM \_ DM \_ NOTINTERLACED.

## <a name="inverse-telecine-settings"></a>Inverse Tele Impostazioni

Per una descrizione del telefono inverso, vedere [To Use Inverse Teletr](to-use-inverse-telecine.md).

Se si imposta la modalità di dinterlacing su WM DM DEINTERLACE INVERSETELE STANDBY, è possibile specificare il modello di teletraccia del primo frame di input chiamando \_ \_ \_ [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). L'impostazione da usare è g \_ wszInitialPatternForInverseTeleinit. Impostare il modello iniziale su uno dei valori seguenti.



| valore                                              | Descrizione                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DISABILITAZIONE DELLA MODALITÀ COERENTE IN WM \_ DM \_ \_ \_ \_ IT                | Specifica che il supporto di input è stato passato attraverso il processo teleteso, ma che i fotogrammi non sono più in un modello prevedibile. Ciò indica in genere che il contenuto multimediale è stato modificato dopo l'elaborazione telegrafia. Quando si usa questa impostazione, il codec tenta di ricostruire i fotogrammi originali in modo proprio. |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ TOP    | Specifica che il primo esempio è il campo superiore del frame AA.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ TOP    | Specifica che il primo esempio è il campo superiore del frame BB.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BC \_ TOP    | Specifica che il primo campione è il primo campo del frame BC.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ TOP    | Specifica che il primo esempio è il campo superiore del frame CD.                                                                                                                                                                                                                                             |
| IL PRIMO FOTOGRAMMA IN CLIP DI WM \_ DM IT È \_ \_ \_ \_ \_ \_ \_ DD \_ TOP    | Specifica che il primo campione è il campo superiore del frame DD.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ BOTTOM | Specifica che il primo esempio è il campo inferiore del frame AA.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ BOTTOM | Specifica che il primo esempio è il campo inferiore del frame BB.                                                                                                                                                                                                                                          |
| IL \_ PRIMO \_ \_ \_ FOTOGRAMMA IN CLIP \_ DI \_ \_ \_ \_ WM DM IT È BC BOTTOM | Specifica che il campo inferiore del frame BC è il primo campione.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ BOTTOM | Specifica che il primo esempio è il campo inferiore del frame CD.                                                                                                                                                                                                                                          |
| IL PRIMO FOTOGRAMMA IN CLIP DI WM \_ DM IT È \_ \_ \_ \_ \_ \_ \_ DD \_ BOTTOM | Specifica che il primo campione è il campo inferiore del frame DD.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> </dl>

 

 





