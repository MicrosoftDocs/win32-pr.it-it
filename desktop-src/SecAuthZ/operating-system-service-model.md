---
description: Un'applicazione in esecuzione come utente standard comunica con un servizio in esecuzione come SYSTEM tramite RPC (Remote Procedure Call).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modello di servizio del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907801"
---
# <a name="operating-system-service-model"></a>Modello di servizio del sistema operativo

Nel modello di servizio del sistema operativo un'applicazione in esecuzione come utente standard comunica con un servizio in esecuzione come **SYSTEM** tramite [RPC (Remote Procedure Call).](/windows/desktop/Rpc/rpc-start-page)

L'applicazione utente standard è contrassegnata nel manifesto dell'applicazione con **requestedExecutionLevel** **di asInvoker**. Per eseguire un'operazione che richiede privilegi di amministratore, l'applicazione utente standard effettua una richiesta al servizio.

Un uso del modello di servizio del sistema operativo è la gestione di applicazioni che potrebbero influire sul sistema, ad esempio antivirus o altri software indesiderati e spyware. L'applicazione utente standard consente all'utente connesso di controllare alcuni aspetti del servizio. Il servizio è responsabile della determinazione delle operazioni eseguite per un'applicazione utente standard. Ad esempio, un servizio antivirus potrebbe consentire a un utente standard di avviare un'analisi del sistema, ma potrebbe non consentire a un utente standard di disabilitare il controllo dei virus in tempo reale.

Un vantaggio principale dell'uso del modello di servizio del sistema operativo è che non è necessaria alcuna richiesta di elevazione dei privilegi.

Uno svantaggio dell'uso del modello di servizio del sistema operativo è che un servizio in esecuzione nel sistema usa più risorse di un'attività e un servizio non può essere arrestato da un utente standard. Se è [sufficiente, è consigliabile](elevated-task-model.md) usare il modello di attività con privilegi elevati.

Per implementare il modello di servizio del sistema operativo, creare un'applicazione client utente standard e un servizio del sistema operativo. Installare il servizio nel sistema operativo durante l'installazione del prodotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello di broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello a oggetti COM amministratore](administrator-com-object-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> </dl>

 

 
