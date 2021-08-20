---
title: Panoramica di Windows Media DRM
description: Panoramica di Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- digital rights management (DRM), informazioni
- DRM (Digital Rights Management),informazioni
- digital rights management (DRM), creazione di pacchetti Windows file multimediali
- DRM (Digital Rights Management),creazione di pacchetti Windows file multimediali
- digital rights management (DRM), licenze file protette
- DRM (Digital Rights Management),gestione delle licenze file protette
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- digital rights management (DRM), lettura di file protetti
- DRM (Digital Rights Management),lettura di file protetti
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format),Digital Rights Management (DRM)
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6cc882d31873a05361869b9246da1b57ac3d3aebb85073d0b31f24509a615b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846416"
---
# <a name="overview-of-windows-media-drm"></a>Panoramica di Windows Media DRM

Windows Media Digital Rights Management (DRM) è un sistema per la protezione del contenuto nei file multimediali di Windows in modo che gli utenti non autorizzati non possono accedervi. Il ciclo DRM di base è in tre fasi: creazione di pacchetti, licenze e lettura.

## <a name="packaging-windows-media-files"></a>Creazione di Windows file multimediali

Windows Media DRM è progettato per funzionare con Windows file multimediali. Un file Windows Media è un file conforme alla specifica ASF (Advanced Systems Format) e contiene solo audio e video compressi usando i codec audio e video di Windows Media.

Quando un file ASF viene in pacchetto, all'intestazione viene aggiunta una sezione specifica di DRM. L'intestazione DRM contiene un ID chiave, che identifica il contenuto ai fini delle licenze, e un URL di acquisizione delle licenze, ovvero l'indirizzo di una pagina Web che può rilasciare licenze per leggere il contenuto protetto. Sono disponibili molte altre informazioni che è possibile inserire nell'intestazione DRM, ma sono facoltative. L'intestazione DRM è firmata in modo che sia possibile verificare il packager.

Il contenuto nel file ASF viene crittografato durante il processo di creazione di un pacchetto. Tuttavia, le informazioni seguenti nel file in pacchetto sono disponibili anche per i client che non hanno una licenza:

-   Metadati archiviati nell'intestazione ASF.
-   Alcuni metadati archiviati nell'intestazione DRM( ad esempio, è sempre possibile ottenere l'URL di acquisizione della licenza).

## <a name="licensing-protected-files"></a>Gestione delle licenze per i file protetti

Per la lettura di un file in pacchetto, è necessario emessa una licenza per il computer client. Una licenza è un set di dati che descrive le condizioni in cui è possibile leggere i dati nei file protetti. Nella maggior parte dei casi, viene rilasciata una licenza per un file protetto in risposta all'utente che tenta di eseguire un'operazione sul file. È anche possibile, tuttavia, che un emittente di licenze consegne le licenze a un client prima che venga richiesto in modo esplicito. Per altre informazioni sulle licenze, vedere [Licenze.](licenses.md)

## <a name="reading-data-from-protected-files"></a>Lettura di dati da file protetti

Quando un utente tenta di eseguire un'operazione su un file protetto (riproduzione, masterizzazione su CD, copia in un dispositivo e così via), l'applicazione deve verificare la presenza di licenze per il contenuto nel computer client. Se nel computer client esiste una licenza valida, l'operazione può continuare. Se non è disponibile una licenza per il contenuto o se nessuna licenza per il contenuto presente nel computer client consente l'azione richiesta, è necessario acquisire una licenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle WINDOWS client Media DRM estese**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




