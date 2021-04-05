---
title: Sottotipi di supporti non compressi
description: Sottotipi di supporti non compressi
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows Media Format SDK, tipi di supporto
- Formati di sistemi avanzati (ASF), tipi di supporto
- ASF (formato di sistemi avanzati), tipi di supporto
- Windows Media Format SDK, sottotipi di supporti non compressi
- Formati di sistemi avanzati (ASF), sottotipi di supporti non compressi
- ASF (Advanced Systems Format), sottotipi di supporti non compressi
- tipi di supporto, sottotipi di supporti non compressi
- sottotipi di supporti non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7ea730b480f738caa6e0eeccb8674f3cdc4c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709598"
---
# <a name="uncompressed-media-subtypes"></a>Sottotipi di supporti non compressi

Nella tabella seguente sono elencati i sottotipi di supporti non compressi. Si tratta di tipi usati come formati di input e di output e formati per i flussi non compressi. Non tutti i tipi nelle tabelle seguenti sono supportati in tutti i modi. I tipi di formato di input e output supportati possono essere enumerati in base al codec rispettivamente nel writer e nel lettore sincrono. Per informazioni sui tipi supportati per i flussi non compressi, vedere [uso di flussi audio e video non compressi](using-uncompressed-audio-and-video-streams.md).

I vari tipi di video RGB RGB e pallettizzati elencati qui definiscono i colori usando il formato RGB, in cui ogni colore è rappresentato dai valori di intensità dei componenti rosso, verde e blu del pixel. Ogni valore di intensità può variare da 0 a 255, per circa 16.780.000 colori univoci. RGB si traduce facilmente in valori di colore utilizzati per i monitor computer, che utilizzano fosfori rosso, verde e blu per visualizzare il colore. I tipi di video pallettizzati devono includere le informazioni sulla tavolozza direttamente dopo la struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) . Analogamente, il video a 16 bit richiede informazioni sui campi di bit che devono essere incluse dopo la struttura WMVIDEOINFOHEADER.

Diversi sottotipi di supporti nella tabella seguente forniscono un numero di colori inferiore a quello supportato dal sistema RGB, come descritto nella colonna Descrizione. Nei tipi pallettizzati RGB i colori della tavolozza rappresentano valori RGB, ma sono specificati da un valore che indica la posizione del colore nella tavolozza.



| Sottotipo di supporto non compresso | Descrizione                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RGB1 WMMEDIASUBTYPE       | Video pallettizzati RGB con 1 bit di colore che rappresenta 2 colori. Usato in genere per le immagini monocromatiche.                                                                                                                         |
| \_RGB4 WMMEDIASUBTYPE       | Video pallettizzati RGB con 4 bit di colore che rappresentano 16 colori.                                                                                                                                                           |
| \_RGB8 WMMEDIASUBTYPE       | Video pallettizzati RGB con 8 bit di colore che rappresentano 256 colori.                                                                                                                                                          |
| \_RGB565 WMMEDIASUBTYPE     | Video RGB con 16 bit di colore che rappresentano 65.536 colori. Questo formato USA 5 bit per il rosso, 6 bit per il verde e 5 bit per il blu.                                                                                         |
| \_RGB555 WMMEDIASUBTYPE     | Video RGB con 16 bit di colore che rappresentano 32.768 colori. Questo formato USA 5 bit per ogni colore e ignora il sedicesimo bit.                                                                                           |
| \_RGB24 WMMEDIASUBTYPE      | Video RGB con 24 bit di colore che rappresentano tutti i colori 16.777.216 disponibili per lo schema di rappresentazione colori RGB. Questo formato USA 8 bit per ogni valore di intensità del colore.                                                |
| \_Rgb32 WMMEDIASUBTYPE      | Video RGB con 32 bit di colore che rappresentano tutti i colori 16.777.216 disponibili per lo schema di rappresentazione colori RGB. Questo formato USA 8 bit per ogni colore e riserva gli 8 bit rimanenti per le informazioni sulla trasparenza. |
| \_I420 WMMEDIASUBTYPE       | Video YUV archiviato in formato Planar 4:2:0, con il piano U che appare per primo, seguito dal piano V.                                                                                                                      |
| \_IYUV WMMEDIASUBTYPE       | Identico a I420.                                                                                                                                                                                                       |
| \_YV12 WMMEDIASUBTYPE       | Video YUV archiviato in formato Planar 4:2:0, con il piano V visualizzato per primo, seguito dal piano U. YV12 è identico a I420 ad eccezione del fatto che i piani di i e V sono stati scambiati.                                               |
| \_YUY2 WMMEDIASUBTYPE       | Video YUV archiviato in formato 4:2:2 compresso.                                                                                                                                                                                 |
| \_UYVY WMMEDIASUBTYPE       | Video YUV archiviato in formato 4:2:2 compresso. Simile a YUY2 ma con un ordine di dati diverso.                                                                                                                            |
| \_YVYU WMMEDIASUBTYPE       | Video YUV archiviato in formato 4:2:2 compresso. Simile a YUY2 ma con un ordine di dati diverso.                                                                                                                            |
| \_P422 WMMEDIASUBTYPE       | Video YUV archiviato con un formato planare 4:2:2.                                                                                                                                                                            |
| \_YVU9 WMMEDIASUBTYPE       | Video YUV archiviato in formato Planar 16:1:1.                                                                                                                                                                                |
| \_PCM WMMEDIASUBTYPE        | Dati audio non compressi archiviati con la modulazione del codice Pulse.                                                                                                                                                              |
| \_DRM WMMEDIASUBTYPE        | Dati audio non compressi ma crittografati usati con il percorso audio protetto.                                                                                                                                                       |
| \_TWOSTRINGS WMSCRIPTTYPE   | Comandi di script costituiti da una stringa contenente il tipo di comando e una stringa contenente i dati del comando. Questo è l'unico tipo di script supportato in Windows Media Format SDK.                                     |
| WMMEDIASUBTYPE \_ webstream  | Dati di trasferimento di file contenenti file e componenti HTML per lo streaming Web.                                                                                                                                               |
| \_VIDEOIMAGE WMMEDIASUBTYPE | Tipo di input per il codec di immagine Windows Media Video 9. Gli esempi sono una combinazione di immagini bitmap e dati di trasformazione.                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Assegnazione di formati di output**](assigning-output-formats.md)
</dt> <dt>

[**Sottotipi di supporti compressi**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificatori del tipo di supporto**](media-type-identifiers.md)
</dt> <dt>

[**Tipi di supporto**](media-types.md)
</dt> <dt>

[**Per enumerare i formati di input**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




