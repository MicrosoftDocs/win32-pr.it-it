---
description: Introduzione ai servizi di modifica DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introduzione ai servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481613"
---
# <a name="introduction-to-directshow-editing-services"></a>Introduzione ai servizi di modifica DirectShow

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il nucleo di DirectShow è un'architettura potente per la gestione dei flussi multimediali. Un'applicazione può usarla per riprodurre contenuti multimediali creati in un'ampia gamma di formati, senza che lo sviluppatore debba preoccuparsi della compressione dei file e di altri dettagli noiosi. Prima di [DirectShow editing Services](directshow-editing-services.md) (des), tuttavia, DirectShow non aveva la flessibilità necessaria per la modifica non lineare.

Si supponga, ad esempio, di voler creare una sequenza video composta da 4 secondi dall'origine A, seguita da 10 secondi dall'origine B, fino a 5 secondi dall'origine C. È possibile eseguire questa operazione in modo molto semplice usando solo l'API DirectShow di base.

Tuttavia, se si è deciso che l'origine C deve precedere l'origine B, non dopo; che la sequenza usi 8 secondi dall'origine A, non 4; e che l'intera produzione avesse bisogno di una traccia audio separata in background? Anche le modifiche minime, ad esempio, potrebbero essere difficili da implementare. Tuttavia, lo scenario appena descritto è un semplice progetto di modifica in DES: è possibile eseguire questa operazione con alcune chiamate al metodo.

Di seguito sono riportate alcune delle funzionalità che DES apporta a DirectShow:

-   Modello di sequenza temporale che organizza tracce video e audio in livelli annidati, semplificando la manipolazione della produzione finale
-   La possibilità di visualizzare in tempo reale un progetto video
-   Persistenza del progetto tramite un formato basato su XML
-   Supporto per effetti audio e video, nonché transizioni tra tracce video, ad esempio dissolvenze e cancellazioni.
-   Oltre 100 salviettine standard, come definito dalla società di Motion Picture and Television Engineers (SMPTE)
-   Digitazione in base a tonalità, luminanza, valore RGB o valore alfa
-   Conversione automatica delle frequenze dei fotogrammi e del campionamento audio, consentendo a un ambiente di produzione di utilizzare origini eterogenee
-   Ridimensionamento o ritaglio di video

Limitazioni

-   DES non supporta le origini video MPEG-2 o H. 264.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi di modifica DirectShow](directshow-editing-services.md)
</dt> </dl>

 

 



