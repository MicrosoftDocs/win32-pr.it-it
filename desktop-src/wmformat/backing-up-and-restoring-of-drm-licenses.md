---
title: Backup e ripristino delle licenze DRM
description: Backup e ripristino delle licenze DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK, backup delle licenze DRM
- Windows Media Format SDK, ripristino delle licenze DRM
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Windows Media Format SDK, funzionalità ripristino backup
- Windows Media Format SDK,License Management Service
- Windows MEDIA Format SDK, rilevamento delle frodi
- digital rights management (DRM), backup delle licenze
- DRM (digital rights management), backup delle licenze
- digital rights management (DRM), ripristino delle licenze
- DRM (digital rights management), ripristino delle licenze
- digital rights management (DRM), licenze
- DRM (digital rights management), licenze
- digital rights management (DRM), funzionalità Ripristino backup
- DRM (digital rights management),funzionalità Ripristino backup
- digital rights management (DRM), License Management Service
- DRM (digital rights management),License Management Service
- digital rights management (DRM), rilevamento delle frodi
- DRM (digital rights management), rilevamento delle frodi
- backup di licenze DRM
- ripristino di licenze DRM
- licenze, DRM
- licenze, backup di DRM
- licenze, ripristino di DRM
- Funzionalità di ripristino del backup
- Servizio gestione licenze
- rilevamento di frodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019163a42312b14b7d7b7e15cea68be1996a976e42b31491f62486a43d37b8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028149"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Backup e ripristino delle licenze DRM

Con la funzionalità Ripristino backup, gli utenti possono eseguire il backup e il ripristino [*delle*](wmformat-glossary.md) licenze nello stesso computer o in altri computer. Questa funzionalità consente agli utenti di trasferire le licenze a un nuovo computer o di nuovo nello stesso computer ,ad esempio dopo la riformattazione del disco rigido. Inoltre, gli utenti possono riprodurre file ASF protetti in più computer.

Per favorire l'uso legittimo di una licenza, i criteri di rilevamento delle frodi limitano il numero di volte in cui è possibile ripristinare una licenza. Microsoft fornisce un servizio che tiene traccia del numero di computer in cui è stata ripristinata una licenza. Se viene raggiunto un limite, l'utente non può ripristinare la licenza.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Consentire o non consentire il diritto di backup e ripristino

La funzionalità Ripristino backup funziona solo per le licenze per le quali è stato assegnato il diritto Backup e ripristino. Se i proprietari di contenuti o gli emittente di licenze non vogliono questa funzionalità o se emettere licenze che contengono uno stato sicuro (ad esempio operazioni conteggiate o tempo limitato), possono non consentire questo diritto.

Quando non è possibile ripristinare una licenza perché un utente non ha il diritto, viene passato un [*ID chiave*](wmformat-glossary.md) all'applicazione. Come minimo, all'utente deve essere notificato che non è stato possibile eseguire il backup di alcune licenze, anche se l'utente non sa a quali licenze fa riferimento questo messaggio. Se si conosce l'ID chiave per i file protetti disponibili, è possibile sviluppare una soluzione più affidabile per informare l'utente.

Ad esempio, un lettore può essere sviluppato per un'etichetta di record che fornisce brani protetti su Internet. Questi brani e i relativi ID chiave possono essere tracciati in un database. Se non è stato possibile eseguire il backup di alcune licenze, l'applicazione lettore potrebbe usare l'ID chiave per eseguire una query sul database per il nome dei brani, quindi informare l'utente per quali brani non è possibile eseguire il backup delle licenze. In caso contrario, è possibile creare una libreria di musica per ogni utente in locale e usare l'ID chiave per recuperare altre informazioni sulle licenze di cui non è stato possibile eseguire il backup.

## <a name="the-license-management-service"></a>Servizio di gestione delle licenze

Quando viene implementata la funzionalità Ripristino backup, un servizio di gestione delle licenze ospitato da Microsoft gestisce il ripristino delle licenze.

In primo luogo, gli utenti esere necessario eseguire il backup delle licenze nell'applicazione, ad esempio scegliendo un'opzione di menu. Il backup di tutte le licenze nel computer viene eseguito in un percorso specificato, ad esempio un disco floppy. Gli utenti ripristinano quindi le licenze usando l'applicazione, ad esempio scegliendo un'opzione di menu e specificando il percorso di backup.

A questo punto, l'utente deve essere connesso a Internet. una richiesta dell'applicazione viene inviata al servizio di gestione delle licenze. Se il computer da cui è stato eseguito il backup della licenza è diverso dal computer originale (o il computer originale è stato riformattato), il Servizio gestione licenze eseghe una nuova licenza al nuovo computer. In caso contrario, viene riemessa la licenza rilasciata in precedenza a tale computer.

Poiché il Servizio gestione licenze recupera informazioni dall'utente, è necessario visualizzare l'informativa sulla privacy Microsoft o fornire un collegamento a tale pagina nel [sito Web Microsoft.](https://www.microsoft.com/licensing/default)

> [!Note]  
> Quando un utente finale ripristina una licenza in un computer diverso e la licenza richiede l'individualizzazione, l'utente finale deve autorizzare i componenti DRM per l'aggiornamento. È necessario implementare un processo nell'applicazione lettore per supportare questa funzionalità.

 

## <a name="detecting-fraud"></a>Rilevamento di frodi

L'utente può ripristinare una licenza per un numero limitato di volte. Ogni volta che una licenza viene ripristinata, il servizio di gestione delle licenze ne tiene traccia e incrementa di uno il conteggio per tale licenza. Quando si ripristina una licenza in un computer in cui la licenza è stata ripristinata in precedenza (ad esempio, il computer da cui è stato eseguito il backup della licenza), il conteggio non viene aumentato. Un computer viene considerato diverso se dispone di un nuovo sistema operativo o se il sistema operativo è stato nuovamente installato.

In conformità ai criteri di rilevamento delle frodi di Microsoft, quando una licenza è stata ripristinata un certo numero di volte, l'applicazione riceve un URL dai componenti DRM ed è responsabile dell'apertura di un browser e della visualizzazione della pagina Web, che indica che il contratto di licenza potrebbe essere stato violato. L'utente deve contattare il distributore di licenze, che deve quindi determinare se la richiesta è valida.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Backup e ripristino delle licenze**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




