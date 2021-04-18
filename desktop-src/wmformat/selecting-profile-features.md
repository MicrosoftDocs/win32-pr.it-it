---
title: Selezione delle funzionalità del profilo
description: Selezione delle funzionalità del profilo
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- profili, selezione delle funzionalità
- profili, selezione funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298101"
---
# <a name="selecting-profile-features"></a>Selezione delle funzionalità del profilo

Nella tabella seguente sono elencate le funzionalità del profilo e viene descritto quando si desidera utilizzarle o meno.



| Funzionalità                            | Utilizzo                                                                                                                                                                                                                                                                                                                | Quando non usare                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esclusione reciproca per velocità in bit (MBR) | Il file verrà trasmesso a un gruppo di destinatari con velocità di connessione diverse da utente a utente, ad esempio file distribuiti su Internet.                                                                                                                                                                              | Il file non verrà trasmesso in rete. Il file verrà trasmesso in una rete con una larghezza di banda disponibile costantemente affidabile (ad esempio, i file distribuiti in una rete locale aziendale).<br/>                                                              |
| Esclusione reciproca per lingua       | Il file contiene flussi che duplicano gli stessi dati in lingue diverse. Ad esempio, un film soprannominato in diversi linguaggi avrebbe codificato come flussi che si escludono a vicenda.                                                                                                                         | Il file contiene solo flussi in una sola lingua. Se il file contiene solo flussi che devono essere modificati per i singoli linguaggi, potrebbe essere più semplice creare un nuovo file per ogni lingua, ad esempio per un film di formazione con un numero elevato di testo nel flusso video.<br/> |
| Esclusione reciproca per presentazione   | Si desidera fornire un video in più proporzioni. Ad esempio, un file potrebbe contenere lo stesso video formattato per la televisione e il formato originale per la visualizzazione a schermo intero.                                                                                                                                     | Esiste una sola versione di ogni flusso video.                                                                                                                                                                                                                                    |
| Condivisione della larghezza di banda                  | Il file verrà trasmesso e avrà due o più flussi che, quando combinati, usano una larghezza di banda minore disponibile rispetto ai valori di velocità in bit di entrambi i flussi aggiunti insieme. Poiché la velocità in bit di un flusso è essenzialmente la massima larghezza di banda necessaria per il flusso, è possibile che alcuni flussi richiedano un trasferimento dati inferiore. | Il file non verrà trasmesso in rete. Tutti i flussi hanno velocità in bit coerenti.<br/>                                                                                                                                                                                     |
| Assegnazione di priorità al flusso              | Il file verrà trasmesso e alcuni flussi sono più importanti di altri.                                                                                                                                                                                                                                                 | Il file non verrà trasmesso in rete. Tutti i flussi sono di uguale importanza.<br/>                                                                                                                                                                                       |
| Estensioni unità dati               | Sono presenti importanti informazioni correlate agli esempi in un flusso che devono essere conservati con gli esempi.                                                                                                                                                                                                                      | Il file deve essere recapitato tramite una larghezza di banda limitata. In questo caso, le estensioni dell'unità dati possono usare un sovraccarico eccessivo.                                                                                                                                                    |



 

Quando si crea un profilo, è inoltre importante prendere in considerazione le funzionalità di codec che si desidera utilizzare con il file. Per altre informazioni, vedere [funzionalità di codec](codec-features.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Progettazione di profili**](designing-profiles.md)
</dt> </dl>

 

 





