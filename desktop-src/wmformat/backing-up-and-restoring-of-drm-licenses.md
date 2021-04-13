---
title: Backup e ripristino di licenze DRM
description: Backup e ripristino di licenze DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK, backup di licenze DRM
- Windows Media Format SDK, ripristino di licenze DRM
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Windows Media Format SDK, funzionalità di ripristino di backup
- Windows Media Format SDK, servizio di gestione delle licenze
- Windows Media Format SDK, rilevamento di frodi
- Digital Rights Management (DRM), backup delle licenze
- DRM (Digital Rights Management), backup delle licenze
- Digital Rights Management (DRM), ripristino di licenze
- DRM (Digital Rights Management), ripristino di licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), funzionalità di ripristino del backup
- DRM (Digital Rights Management), funzionalità di ripristino del backup
- Digital Rights Management (DRM), servizio gestione licenze
- DRM (Digital Rights Management), servizio di gestione delle licenze
- Digital Rights Management (DRM), rilevamento di frodi
- DRM (Digital Rights Management), rilevamento di frodi
- backup di licenze DRM
- ripristino di licenze DRM
- licenze, DRM
- licenze, backup di DRM
- licenze, ripristino di DRM
- Funzionalità Ripristino backup
- Servizio gestione licenze
- rilevamento di frodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104339495"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Backup e ripristino di licenze DRM

Con la funzionalità di ripristino del backup, gli utenti possono eseguire il backup e il ripristino delle [*licenze*](wmformat-glossary.md) nello stesso computer o in altri computer. Questa funzionalità consente agli utenti di trasferire le licenze in un nuovo computer o di nuovo nello stesso computer, ad esempio dopo aver riformattato il disco rigido. Inoltre, gli utenti possono riprodurre file ASF protetti in più di un computer.

Per incoraggiare l'utilizzo legittimo di una licenza, i criteri di rilevamento delle frodi limitano il numero di volte che è possibile ripristinare una licenza. Microsoft fornisce un servizio che tiene traccia del numero di computer a cui è stata ripristinata una licenza; Se viene raggiunto un limite, l'utente non potrà ripristinare la licenza.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Consentire o impedire il diritto di eseguire il backup e il ripristino

La funzionalità di ripristino del backup funziona solo per le licenze per le quali viene assegnato il diritto di backup e ripristino. Se i proprietari del contenuto o le autorità emittenti di licenze non desiderano questa funzionalità o se emettono licenze che contengono uno stato sicuro (ad esempio, operazioni conteggiate o tempo limitato), possono impedire questo diritto.

Quando non è possibile ripristinare una licenza perché un utente non dispone del diritto, all'applicazione viene passato un [*ID chiave*](wmformat-glossary.md) . Come minimo, l'utente deve ricevere una notifica che non è stato possibile eseguire il backup di alcune licenze, anche se l'utente non è in grado di stabilire a quali licenze si riferisce questo messaggio. Se si conosce l'ID chiave per i file protetti disponibili, è possibile sviluppare una soluzione più affidabile per informare l'utente.

Ad esempio, un giocatore può essere sviluppato per un'etichetta di record che fornisce canzoni protette su Internet. È possibile tenere traccia di questi brani e dei relativi ID chiave in un database. Se non è stato possibile eseguire il backup di alcune licenze, l'applicazione lettore può usare l'ID chiave per eseguire una query sul database per il nome dei brani, quindi informare l'utente per quali brani non è possibile eseguire il backup delle licenze. In alternativa, è possibile creare una raccolta musicale per ogni utente localmente e l'ID chiave può essere usato per recuperare altre informazioni sulle licenze di cui non è stato eseguito il backup.

## <a name="the-license-management-service"></a>Il servizio gestione licenze

Quando viene implementata la funzionalità di ripristino del backup, un servizio di gestione delle licenze ospitato da Microsoft gestisce il ripristino delle licenze.

In primo luogo, gli utenti eseguono il backup delle licenze nell'applicazione, ad esempio scegliendo un'opzione di menu. Viene eseguito il backup di tutte le licenze del computer in un percorso specifico, ad esempio un disco floppy. Quindi, gli utenti ripristinano le licenze utilizzando l'applicazione, ad esempio scegliendo un'opzione di menu e specificando il percorso di backup.

A questo punto, l'utente deve essere connesso a Internet. una richiesta dell'applicazione viene inviata al servizio di gestione delle licenze. Se il computer da cui è stato eseguito il backup della licenza è diverso dal computer originale (oppure il computer originale è stato riformattato), il servizio di gestione delle licenze rilascia una nuova licenza per il nuovo computer. In caso contrario, la licenza che è stata rilasciata in precedenza a tale computer viene rilasciata.

Poiché il servizio gestione licenze recupera le informazioni dall'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel [sito Web Microsoft](https://www.microsoft.com/licensing/default).

> [!Note]  
> Quando un utente finale ripristina una licenza in un computer diverso e la licenza richiede l'individualizzazione, l'utente finale deve autorizzare i componenti DRM da aggiornare. Per supportare questa funzionalità, è necessario implementare un processo nell'applicazione del lettore.

 

## <a name="detecting-fraud"></a>Rilevamento di illeciti

L'utente è autorizzato a ripristinare una licenza per un numero limitato di volte. Ogni volta che viene ripristinata una licenza, il servizio di gestione delle licenze lo tiene traccia e incrementa il conteggio di una licenza. Quando si ripristina una licenza in un computer in cui la licenza è stata ripristinata in precedenza (ad esempio, il computer da cui è stato eseguito il backup della licenza), il conteggio non viene aumentato. Un computer viene considerato diverso se dispone di un nuovo sistema operativo o se il sistema operativo è stato reinstallato.

In conformità ai criteri di rilevamento delle frodi di Microsoft, quando una licenza è stata ripristinata un determinato numero di volte, l'applicazione riceve un URL dai componenti DRM ed è responsabile dell'apertura di un browser e della visualizzazione della pagina Web, che indica che il contratto di licenza potrebbe essere stato violato. L'utente deve contattare il distributore di licenze, che deve stabilire se la richiesta è valida.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Backup e ripristino di licenze**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




