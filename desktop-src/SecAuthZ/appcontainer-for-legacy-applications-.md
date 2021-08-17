---
description: L'ambiente AppContainer è un ambiente di esecuzione del processo restrittivo che può essere usato per le applicazioni legacy per garantire la sicurezza delle risorse.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer per applicazioni legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e0cdf21fc4008f1da0d55edb17abaf71978f4a5384843ecff60793b3d5b19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784734"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer per applicazioni legacy

L'ambiente AppContainer è un ambiente di esecuzione del processo restrittivo che può essere usato per le applicazioni legacy per garantire la sicurezza delle risorse. Un'applicazione in esecuzione in un AppContainer può accedere solo alle risorse concesse in modo specifico. Di conseguenza, le applicazioni implementate in un AppContainer non possono essere violate per consentire azioni dannose al di fuori delle risorse assegnate limitate.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Vantaggi dell'uso di un ambiente AppContainer

L'ambiente AppContainer fornisce sandboxing sicuro delle applicazioni. In questo modo l'applicazione non può accedere a hardware, file, Registro di sistema, altre applicazioni, connettività di rete e risorse di rete senza autorizzazioni specifiche. Le singole risorse possono essere destinate senza esporre altre risorse. Inoltre, l'identità utente viene protetta usando un'identità univoca che è una concatenazione dell'utente e l'app e le risorse vengono concesse usando un modello con privilegi minimi. Questo protegge ulteriormente da un'app che rappresenta l'utente per ottenere l'accesso ad altre risorse.

Per altre informazioni sull'uso di AppContainer per applicazioni legacy, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Isolamento di AppContainer](appcontainer-isolation.md)<br/>             | L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer. Isolando un'applicazione da risorse non necessarie e altre applicazioni, le opportunità di manipolazione dannosa sono ridotte al minimo. La concessione dell'accesso in base ai privilegi minimi impedisce alle applicazioni e agli utenti di accedere alle risorse oltre i propri diritti. Il controllo dell'accesso alle risorse protegge il processo, il dispositivo e la rete.<br/> |
| [Implementazione di un AppContainer](implementing-an-appcontainer.md)<br/> | Un AppContainer viene implementato aggiungendo nuove informazioni al token di processo, modificando [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) in modo che tutti gli oggetti legacy non modificati dell'elenco di controllo di accesso (ACL) blocchino le richieste di accesso dai processi di AppContainer per impostazione predefinita e gli oggetti re-ACL che devono essere disponibili per AppContainers.<br/>                                                                                        |



 

 

