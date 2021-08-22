---
description: Introduzione ai DirectShow di modifica
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introduzione ai DirectShow di modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d12470b45e0b39c32c983176f07444a5136b9e97b99cc5be142974d05178f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952549"
---
# <a name="introduction-to-directshow-editing-services"></a>Introduzione ai DirectShow di modifica

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Il nucleo di DirectShow è un'architettura potente per la gestione dei supporti di streaming. Un'applicazione può usarla per riprodurre contenuto multimediale creato in un'ampia gamma di formati, senza che lo sviluppatore si preoccupa della compressione dei file e di altri dettagli noiosi. Prima di [DirectShow Editing Services](directshow-editing-services.md) (DES), tuttavia, DirectShow la flessibilità necessaria per la modifica non lineare.

Si supponga, ad esempio, di voler creare una sequenza video costituita da 4 secondi dall'origine A, seguiti da 10 secondi dall'origine B e che terminano con 5 secondi dall'origine C. È possibile eseguire questa operazione molto facilmente usando solo l'API di DirectShow core.

Ma cosa succede se si decide che l'origine C deve essere prima dell'origine B, non dopo; che la sequenza deve usare 8 secondi dall'origine A, non 4; e che l'intera produzione ha bisogno di una traccia audio separata riprodotta in background? Anche modifiche minori come queste potrebbero essere difficili da implementare. Ma lo scenario appena descritto è un progetto di modifica semplice in DES, che è possibile eseguire con un numero limitato di chiamate al metodo.

Ecco alcune delle funzionalità che DES offre a DirectShow:

-   Un modello di sequenza temporale che organizza le tracce audio e video in livelli annidati, semplificando la modifica della produzione finale
-   Possibilità di visualizzare in anteprima un progetto video in tempo reale
-   Project persistenza tramite un formato basato su XML
-   Supporto per gli effetti video e audio, nonché transizioni tra tracce video (ad esempio dissolvenze e cancellazioni)
-   Oltre 100 cancellazioni standard, come definito da SMPTE (Society of Motion Picture and Engineers)
-   Keying basato su tonalità, luminance, valore RGB o valore alfa
-   Conversione automatica delle frequenze dei fotogrammi e delle frequenze di campionamento audio, consentendo a un ambiente di produzione di usare origini eterogenee
-   Ridimensionamento o ritaglio del video

Limitazioni

-   DES non supporta le origini video MPEG-2 o H.264.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Modifica dei servizi](directshow-editing-services.md)
</dt> </dl>

 

 



