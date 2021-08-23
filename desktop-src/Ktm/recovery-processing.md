---
description: Dopo qualsiasi tipo di errore che interrompe la normale elaborazione delle transazioni, KTM e ogni gestore delle risorse devono eseguire operazioni di ripristino. Il ripristino è il processo in base al quale i partecipanti alla transazione arrivano a una visualizzazione coerente dello stato di ogni transazione.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Elaborazione del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec99ad63d18c95da3ebb3ad5db6c204301d75336cc1842dd21e1edf79f5f9a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146494"
---
# <a name="recovery-processing"></a>Elaborazione del ripristino

Dopo qualsiasi tipo di errore che interrompe la normale elaborazione delle transazioni, KTM e ogni gestore delle risorse devono eseguire *operazioni di* ripristino. Il ripristino è il processo in base al quale i partecipanti alla transazione arrivano a una visualizzazione coerente dello stato di ogni transazione.

I gestori delle risorse possono essere *in* dubbio sul risultato di una transazione, vale a dire che al momento dell'errore avevano ricevuto una notifica TRANSACTION NOTIFY PREPARE, si erano preparati per l'archiviazione durevole, ma non avevano ricevuto (o ricevuto ma non registrato) un risultato finale per la \_ transazione. \_ Analogamente, KTM può essere in dubbio su una transazione se è stata preparata ma non ha ricevuto (o ricevuto ma non registrato) un risultato. In fase di ripristino, tutti i risultati inviati ma non riconosciuti devono essere inviati nuovamente. Ad esempio, se un gestore delle risorse ha ricevuto una notifica TRANSACTION NOTIFY COMMIT e ha chiamato la funzione \_ \_ [**CommitComplete,**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) l'RM potrebbe comunque ricevere una notifica TRANSACTION NOTIFY COMMIT duplicata in fase \_ \_ di ripristino.

Per il corretto ripristino di una transazione dopo un errore di sistema o di gestione delle risorse, ogni gestore delle risorse deve eseguire le operazioni seguenti ogni volta che viene avviata:

1.  Chiamare la [**funzione OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) per aprire nuovamente l'handle di gestione risorse usando il nome univoco e permanente. In questo modo KTM informa che gestione risorse è di nuovo in esecuzione ed è disponibile per eseguire il ripristino. Se non sono presenti integrazioni da recuperare, la chiamata a **OpenResourceManager** può avere esito negativo. Chiamare [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) per creare nuovamente l'oggetto RM.
2.  Chiamare [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager). Il gestore delle risorse riceverà un evento di notifica [**TRANSACTION \_ NOTIFY \_ RECOVER**](notification-mask.md) per ogni integrazione per cui deve eseguire operazioni di ripristino, seguita da TRANSACTION \_ NOTIFY LAST \_ \_ RECOVER. L'evento di notifica include un identificatore univoco globale sia per la transazione che per l'integrazione.
3.  Chiamare la [**funzione OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) per aprire nuovamente ogni handle di integrazione per cui il gestore delle risorse ha ricevuto una notifica TRANSACTION \_ NOTIFY \_ RECOVER.
4.  Per ogni integrazione aperta da [**OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)chiamare [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). In questo modo la notifica TRANSACTION NOTIFY COMMIT o \_ \_ TRANSACTION NOTIFY \_ \_ INDOUBT viene rieliverata.
5.  Se l'RM ha ricevuto TRANSACTION \_ NOTIFY COMMIT, l'RM può completare \_ la transazione chiamando [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Se l'RM ha ricevuto TRANSACTION \_ NOTIFY \_ INDOUBT, l'RM deve attendere l'arrivo della notifica del risultato.

6.  Per tutte le transazioni per cui l'RM non riceve una notifica TRANSACTION NOTIFY RECOVER, ma per cui in precedenza ha ricevuto una notifica \_ \_ TRANSACTION NOTIFY \_ PREPARE, l'RM deve elaborare la transazione come se ne fosse eseguito il \_ rollback.

> [!Note]
>
> I responsabili delle risorse possono integrare o creare nuove transazioni durante il processo di esecuzione del ripristino.

 

KTM usa un modello *di transazione di interruzione* presunto. Lo scenario seguente illustra questo comportamento. Si supponga che KTM e un gestore delle risorse esistano nello stesso computer. Si supponga che KTM eserciti una notifica di preparazione per una transazione, ma che il sistema si arresti in modo anomalo prima che KTM registri la notifica di preparazione. Si supponga inoltre che gestione risorse riceva e registri la notifica di preparazione subito prima che il sistema si arresti in modo anomalo. Dopo il ripristino del sistema, KTM non è a conoscenza della transazione, perché non ha mai registrato la fase di preparazione. Il gestore delle risorse è a conoscenza della transazione, perché ha ricevuto, elaborato e registrato la notifica di preparazione. Quando KTM invia le notifiche di ripristino, il gestore delle risorse non include una notifica di ripristino per la transazione in questione. Con il modello di interruzione presunto, il gestore delle risorse in questo caso tratterà la transazione preparata come interrotta quando non riceve notifiche per eseguire il ripristino su tale transazione.

 

 



