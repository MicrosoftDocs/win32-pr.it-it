---
description: Se si scrive un servizio o un componente ed è necessario usare servizi transazionali o se è necessario monitorare lo stato di una transazione del kernel, è necessario creare un gestore di risorse (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Scrittura di un Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b1443bef61f56a14779612a6275aacbd65e344d7294325bd87b953795f0f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086451"
---
# <a name="writing-a-resource-manager"></a>Scrittura di un Resource Manager

Se si scrive un servizio o un componente ed è necessario usare servizi transazionali o se è necessario monitorare lo stato di una transazione del kernel, è necessario creare un gestore di risorse (RM).

Per scrivere un gestore di risorse, è necessario creare più oggetti kernel. Gli oggetti utilizzati da un RM sono:

-   Oggetti di gestione transazioni (TM)
-   Resource Manager oggetti
-   Oggetti di integrazione

Creare prima di tutto un oggetto TM. Esistono due tipi di TM:

-   Volatile: queste macchine virtuali non hanno un log e non possono ripristinare il proprio stato
-   Durevole: queste macchine virtuali hanno un log

Per creare un TM durevole, è necessario creare un log CLFS e chiamare [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) oppure fare in modo che KTM lo crei automaticamente. Dopo aver creato un TM durevole, è necessario innanzitutto ripristinare il TM chiamando [**RecoverTransactionManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) Dopo il ripristino, il TM è disponibile per l'uso.

Se è stato ripristinato un TM esistente, tutte le macchine virtuali associate a questa TM inizieranno a ricevere messaggi di ripristino. Per altre informazioni, vedere [Elaborazione del ripristino.](recovery-processing.md)

Creare quindi un gestore di risorse chiamando [**CreateResourceManager con**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) l'handle TM. L'RM può essere volatile o durevole. Solo le macchine virtuali durevoli possono essere usate con macchine virtuali durevoli.

Quando si lavora in modo transazionale, è possibile integrarsi nella transazione chiamando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e specificando le notifiche da ricevere.

**Nota**  È possibile iniziare a ricevere notifiche prima del [**completamento della chiamata a CreateEnlistment.**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)

Quando si riceve una notifica, chiamare la funzione appropriata "Completa" quando viene completata qualsiasi operazione associata \* all'elaborazione della notifica. Le funzioni complete sono:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Se in qualsiasi momento un gestore di risorse non è in grado di completare il lavoro della transazione o se continuare rende l'applicazione in grado di annullare le operazioni eseguite all'interno della transazione, è necessario eseguire il rollback della transazione chiamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



