---
title: Sottotipi di supporti non compressi
description: Sottotipi di supporti non compressi
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows MEDIA Format SDK, tipi di supporti
- Advanced Systems Format (ASF), tipi di supporti
- ASF (Advanced Systems Format),tipi di supporti
- Windows Media Format SDK, sottotipi di supporti non compressi
- Advanced Systems Format (ASF), sottotipi di supporti non compressi
- ASF (Advanced Systems Format), sottotipi di supporti non compressi
- tipi di supporti, sottotipi di supporti non compressi
- sottotipi di supporti non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807341"
---
# <a name="uncompressed-media-subtypes"></a>Sottotipi di supporti non compressi

Nella tabella seguente sono elencati i sottotipi di supporti non compressi. Si tratta di tipi usati come formati di input e output e di formati per i flussi non compressi. Non tutti i tipi nelle tabelle seguenti sono supportati in tutti i modi. I tipi di formato di input e output supportati possono essere enumerati in base al codec rispettivamente nel writer e nel lettore/lettore sincrono. Per informazioni sui tipi supportati per i flussi non compressi, vedere [Using Uncompressed Audio and Video Flussi](using-uncompressed-audio-and-video-streams.md).

I vari tipi di video RGB e RGB satizzati elencati qui definiscono i colori usando il formato RGB, in cui ogni colore è rappresentato dai valori di intensità dei componenti rosso, verde e blu del pixel. Ogni valore di intensità può variare da 0 a 255, per circa 16,78 milioni di colori univoci. RGB si traduce facilmente in valori di colore usati per i monitor dei computer, che usano phosphor rosso, verde e blu per visualizzare il colore. I tipi di video a colori devono includere informazioni sulla tavolozza direttamente dopo la [**struttura WMVIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) Analogamente, il video a 16 bit richiede informazioni sui campi di bit, che devono essere incluse dopo la struttura WMVIDEOINFOHEADER.

Molti sottotipi multimediali nella tabella seguente forniscono meno colori di quelli che il sistema RGB è in grado di supportare, come descritto nella colonna Descrizione. Nei tipi RGB a colori, i colori nella tavolozza rappresentano valori RGB, ma vengono specificati da un valore che indica la posizione del colore nella tavolozza.



| Sottotipo di supporti non compressi | Descrizione                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Video RGB a tema con 1 bit di colore che rappresenta 2 colori. Usato in genere per immagini monocroma.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Video RGB a tema con 4 bit di colore che rappresentano 16 colori.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Video RGB a tema con 8 bit di colore che rappresentano 256 colori.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Video RGB con 16 bit di colore che rappresentano 65.536 colori. Questo formato usa 5 bit per il rosso, 6 bit per il verde e 5 bit per il blu.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Video RGB con 16 bit di colore che rappresentano 32.768 colori. Questo formato usa 5 bit per ogni colore e ignora il sedicesimo bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | Video RGB con 24 bit di colore che rappresentano tutti i 16.777.216 colori disponibili per lo schema di rappresentazione dei colori RGB. Questo formato usa 8 bit per ogni valore di intensità del colore.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Video RGB con 32 bit di colore che rappresentano tutti i 16.777.216 colori disponibili per lo schema di rappresentazione dei colori RGB. Questo formato usa 8 bit per ogni colore e riserva gli 8 bit rimanenti per le informazioni sulla trasparenza. |
| WMMEDIASUBTYPE \_ I420       | Video YUV archiviato in formato planare 4:2:0, con il piano U visualizzato per primo, seguito dal piano V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Identico a I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Video YUV archiviato in formato planare 4:2:0, con il piano V visualizzato per primo, seguito dal piano U. YV12 è identico a I420, ad eccezione del fatto che i piani you e V vengono commutati.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Video YUV archiviato in formato 4:2:2.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Video YUV archiviato in formato 4:2:2. Simile a YUY2 ma con un ordinamento diverso dei dati.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Video YUV archiviato in formato 4:2:2. Simile a YUY2 ma con un ordinamento diverso dei dati.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Video YUV archiviato in un formato planare 4:2:2.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | Video YUV archiviato in formato planare 16:1:1.                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | Dati audio non compressi archiviati usando la modulazione del codice di pulsazione.                                                                                                                                                              |
| WMMEDIASUBTYPE \_ DRM        | Dati audio non compressi ma crittografati usati con un percorso audio sicuro.                                                                                                                                                       |
| TwoString WMSCRIPTTYPE \_   | Comandi script costituiti da una stringa contenente il tipo di comando e da una stringa contenente i dati del comando. Questo è l'unico tipo di script supportato in Windows Media Format SDK.                                     |
| WMMEDIASUBTYPE \_ WebStream  | Dati di trasferimento di file contenenti file e componenti HTML per il flusso Web.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Tipo di input per il codec Windows Media Video 9 Image. Gli esempi sono una combinazione di immagini bitmap e dati di trasformazione.                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Assegnazione di formati di output**](assigning-output-formats.md)
</dt> <dt>

[**Sottotipi di supporti compressi**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificatori dei tipi di supporti**](media-type-identifiers.md)
</dt> <dt>

[**Tipi di supporti**](media-types.md)
</dt> <dt>

[**Per enumerare i formati di input**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




