---
description: Un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come sistema utilizzando RPC (Remote Procedure Call).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modello di servizio del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967891"
---
# <a name="operating-system-service-model"></a>Modello di servizio del sistema operativo

Nel modello del servizio del sistema operativo, un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come **sistema** utilizzando RPC ( [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) ).

L'applicazione utente standard è contrassegnata nel manifesto dell'applicazione con un **requestedExecutionLevel** di **asInvoker**. Per eseguire un'operazione che richiede privilegi di amministratore, l'applicazione utente standard effettua una richiesta al servizio.

Un utilizzo del modello di servizio del sistema operativo è quello di gestire le applicazioni che potrebbero avere un effetto sul sistema, ad esempio antivirus o altro software indesiderato e spyware. L'applicazione utente standard consente all'utente connesso di controllare alcuni aspetti del servizio. Il servizio è responsabile di determinare le operazioni eseguite per un'applicazione utente standard. Ad esempio, un servizio antivirus potrebbe consentire a un utente standard di avviare un'analisi del sistema, ma potrebbe non consentire a un utente standard di disabilitare il controllo dei virus in tempo reale.

Un vantaggio principale dell'utilizzo del modello di servizio del sistema operativo è che non è richiesta alcuna richiesta di elevazione dei privilegi.

Uno svantaggio dell'uso del modello del servizio del sistema operativo è che un servizio in esecuzione nel sistema usa più risorse di un'attività e un servizio non può essere arrestato da un utente standard. Se è sufficiente, provare a usare il [modello di attività con privilegi elevati](elevated-task-model.md) .

Per implementare il modello di servizio del sistema operativo, creare un'applicazione client utente standard e un servizio del sistema operativo. Installare il servizio nel sistema operativo durante l'installazione del prodotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello di broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello a oggetti COM dell'amministratore](administrator-com-object-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> </dl>

 

 
