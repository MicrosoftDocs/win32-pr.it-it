---
description: L'ambiente AppContainer è un ambiente di esecuzione dei processi restrittivo che può essere usato per le applicazioni legacy per garantire la sicurezza delle risorse.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer per le applicazioni legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b25ea292bdb8935375e50f669d17deb7efaef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319402"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer per le applicazioni legacy

L'ambiente AppContainer è un ambiente di esecuzione dei processi restrittivo che può essere usato per le applicazioni legacy per garantire la sicurezza delle risorse. Un'applicazione in esecuzione in un AppContainer può accedere solo alle risorse concesse in modo specifico. Di conseguenza, non è possibile hackerare le applicazioni implementate in un AppContainer per consentire azioni dannose al di fuori delle risorse assegnate limitate.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Vantaggi dell'uso di un ambiente AppContainer

L'ambiente AppContainer fornisce un sandbox sicuro delle applicazioni. Questo consente di isolare l'applicazione dall'accesso a hardware, file, registro di sistema, altre applicazioni, connettività di rete e risorse di rete senza autorizzazioni specifiche. Le singole risorse possono essere destinate senza esporre altre risorse. Inoltre, l'identità utente è protetta usando un'identità univoca che è una concatenazione dell'utente e l'app e le risorse vengono concesse usando un modello con privilegi minimi. Questa operazione protegge ulteriormente da un'app che rappresenta l'utente per ottenere l'accesso ad altre risorse.

Per ulteriori informazioni sull'utilizzo di AppContainer per le applicazioni legacy, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Isolamento AppContainer](appcontainer-isolation.md)<br/>             | L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer. Isolando un'applicazione da risorse non necessarie e da altre applicazioni, le opportunità di manipolazione dannosa sono ridotte al minimo. Se si concede l'accesso in base al privilegio minimo, le applicazioni e gli utenti non possono accedere alle risorse oltre i rispettivi diritti. Il controllo dell'accesso alle risorse protegge il processo, il dispositivo e la rete.<br/> |
| [Implementazione di un AppContainer](implementing-an-appcontainer.md)<br/> | Un AppContainer viene implementato mediante l'aggiunta di nuove informazioni al token del processo, modificando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) in modo che tutti gli oggetti legacy, non modificati (ACL) di controllo di accesso blocchino le richieste di accesso dai processi appcontainer per impostazione predefinita e gli oggetti ACL che devono essere disponibili per AppContainers.<br/>                                                                                        |



 

 

