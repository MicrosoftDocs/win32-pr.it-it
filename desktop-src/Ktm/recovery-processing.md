---
description: Dopo qualsiasi tipo di errore che interrompe la normale elaborazione delle transazioni, KTM e ogni Resource Manager devono eseguire operazioni di ripristino. Il ripristino è il processo mediante il quale i partecipanti alle transazioni arrivano a una visualizzazione coerente di ogni stato delle transazioni.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Elaborazione del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311134"
---
# <a name="recovery-processing"></a>Elaborazione del ripristino

Dopo qualsiasi tipo di errore che interrompe la normale elaborazione delle transazioni, KTM e ogni Resource Manager devono eseguire operazioni di *ripristino* . Il ripristino è il processo mediante il quale i partecipanti alle transazioni arrivano a una visualizzazione coerente dello stato di ogni transazione.

I gestori di risorse potrebbero non essere *in dubbio* sul risultato di una transazione, vale a dire che, al momento dell'errore, hanno ricevuto una \_ \_ notifica di preparazione alla transazione per la notifica, si è preparata per l'archiviazione durevole, ma non ha ricevuto (o ricevuto ma non registrato) un risultato finale per la transazione. Analogamente, è possibile che KTM sia in dubbio su una transazione se è stata preparata, ma non ha ricevuto (o ricevuto ma non registrato) un risultato. Al momento del ripristino, è necessario inviare nuovamente tutti i risultati inviati ma non riconosciuti. Se, ad esempio, un gestore di risorse ha ricevuto una \_ notifica di commit Transaction Notify \_ e ha chiamato la funzione [**COMMITCOMPLETE**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , il RM potrebbe ancora ricevere una notifica di commit delle transazioni duplicata \_ \_ al momento del ripristino.

Per eseguire correttamente il ripristino di una transazione dopo un errore di sistema o di Resource Manager, ogni gestore di risorse deve eseguire le operazioni seguenti ogni volta che viene avviato:

1.  Chiamare la funzione [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) per riaprire l'handle di Resource Manager usando il nome univoco e permanente. In questo modo, si informa che Gestione risorse è in esecuzione nuovamente ed è disponibile per eseguire il ripristino. Se non è presente alcun elenco per il ripristino, la chiamata a **OpenResourceManager** può avere esito negativo. Chiamare [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) per ricreare l'oggetto RM.
2.  Chiamare [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager). Resource Manager riceverà un evento di notifica della notifica di transazione per ogni integrazione per cui è necessario eseguire operazioni di ripristino, seguito da un ultimo ripristino della notifica della transazione [**\_ \_**](notification-mask.md) \_ \_ \_ . L'evento di notifica include un identificatore univoco globale sia per la transazione che per l'integrazione.
3.  Chiamare la funzione [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) per riaprire ogni handle di integrazione per il quale il gestore di risorse ha ricevuto una notifica di recupero della notifica di transazione \_ \_ .
4.  Per ogni integrazione aperta da [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment), chiamare [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). \_ \_ \_ In questo \_ modo verrà recapitata la notifica del commit della notifica della transazione o della notifica della transazione.
5.  Se il RM ha ricevuto una \_ notifica \_ di transazione, il RM può completare la transazione chiamando [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Se il RM ha ricevuto una \_ notifica \_ di transazione indubbia, il RM deve attendere l'arrivo della notifica di risultato.

6.  Per tutte le transazioni che RM non riceve una notifica di \_ ripristino della transazione \_ , ma che in precedenza ha ricevuto una \_ \_ notifica di preparazione della transazione per, il RM deve elaborare la transazione come se fosse stato eseguito il rollback.

> [!Note]
>
> I gestori di risorse possono eseguire l'integrazione o creare nuove transazioni durante il processo di recupero.

 

KTM utilizza un modello *presunto* di transazione di interruzione. Questo comportamento viene illustrato nello scenario seguente. Si supponga che KTM e uno strumento di gestione delle risorse esistano nello stesso computer. Si supponga che KTM verifichi una notifica di preparazione per una transazione, ma il sistema si arresta in modo anomalo prima che KTM registri la notifica di preparazione. Si supponga inoltre che Resource Manager riceva e registri la notifica di preparazione immediatamente prima che il sistema si arresti in modo anomalo. Una volta ripristinato il sistema, KTM non conosce la transazione, perché non ha mai registrato la fase di preparazione. Resource Manager conosce la transazione, perché ha ricevuto, elaborato e registrato la notifica di preparazione. Quando KTM rilascia le notifiche di ripristino, Resource Manager non include una notifica di ripristino per la transazione in questione. Con il modello di interruzione presunto, gestione risorse in questo caso considererà la transazione preparata come interrotta quando non riceve le notifiche per eseguire il ripristino su tale transazione.

 

 



