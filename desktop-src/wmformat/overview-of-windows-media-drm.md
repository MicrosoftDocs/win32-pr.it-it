---
title: Panoramica di Windows Media DRM
description: Panoramica di Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), informazioni
- DRM (Digital Rights Management), informazioni
- Digital Rights Management (DRM), creazione di pacchetti di file Windows Media
- DRM (Digital Rights Management), creazione di pacchetti di file Windows Media
- Digital Rights Management (DRM), licenze file protette
- DRM (Digital Rights Management), licenze file protette
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), lettura di file protetti
- DRM (Digital Rights Management), lettura di file protetti
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- ASF (formato avanzato dei sistemi), Digital Rights Management (DRM)
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297835"
---
# <a name="overview-of-windows-media-drm"></a>Panoramica di Windows Media DRM

Windows Media Digital Rights Management (DRM) è un sistema per la protezione del contenuto nei file di Windows Media, in modo che gli utenti non autorizzati non possano accedervi. Il ciclo DRM di base prevede tre fasi: creazione di pacchetti, licenze e lettura.

## <a name="packaging-windows-media-files"></a>Creazione di pacchetti di file Windows Media

Windows Media DRM è progettato per funzionare con i file di Windows Media. Un file di Windows Media è un file che è conforme alla specifica ASF (Advanced Systems Format) e contiene solo audio e video compressi con i codec Windows Media Audio e video.

Quando si crea un pacchetto di un file ASF, all'intestazione viene aggiunta una sezione specifica di DRM. L'intestazione DRM contiene un ID chiave, che identifica il contenuto a scopo di gestione delle licenze e un URL di acquisizione della licenza, ovvero l'indirizzo di una pagina Web che può emettere licenze per la lettura del contenuto protetto. Sono disponibili molte altre informazioni che possono essere inserite nell'intestazione DRM, ma è facoltativa. L'intestazione DRM è firmata in modo che sia possibile verificare il pacchetto.

Il contenuto del file ASF viene crittografato durante il processo di compressione. Tuttavia, le informazioni riportate di seguito nel file in pacchetto sono disponibili anche per i client che non dispongono di una licenza:

-   Metadati archiviati nell'intestazione ASF.
-   Alcuni metadati archiviati nell'intestazione DRM (ad esempio, è sempre possibile ottenere l'URL di acquisizione della licenza).

## <a name="licensing-protected-files"></a>File protetti con licenza

Per la lettura di un file in pacchetto, è necessario emettere una licenza per il computer client. Una licenza è un set di dati che descrive le condizioni in base alle quali è possibile leggere i dati nei file protetti. In genere, viene emessa una licenza per un file protetto in risposta all'utente che tenta di eseguire un'operazione sul file. È anche possibile, tuttavia, che un emittente di licenze fornisca licenze a un client prima che venga richiesto in modo esplicito. Per ulteriori informazioni sulle licenze, vedere [licenze](licenses.md).

## <a name="reading-data-from-protected-files"></a>Lettura di dati da file protetti

Quando un utente tenta di eseguire un'operazione su un file protetto (riproduzione, masterizzazione su CD, copia in un dispositivo e così via), l'applicazione deve verificare la presenza di licenze per il contenuto nel computer client. Se nel computer client è presente una licenza valida, l'operazione può proseguire. Se non è disponibile una licenza per il contenuto o se nessuna licenza per il contenuto presente nel computer client consente l'azione richiesta, è necessario acquisire una licenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle API estese del client Windows Media DRM**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




