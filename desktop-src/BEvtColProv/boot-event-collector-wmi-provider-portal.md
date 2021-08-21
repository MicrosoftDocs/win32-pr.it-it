---
description: Il provider WMI dell'agente di raccolta eventi di avvio fornisce l'accesso alle informazioni di connessione e configurazione per la funzionalità Raccolta eventi di installazione e avvio Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Provider WMI dell'agente di raccolta eventi di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccebb4c4408aaa0ce58ad6ab412e4ca85fbb291c8da14ba764dfe3b19e2cbfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579861"
---
# <a name="boot-event-collector-wmi-provider"></a>Provider WMI dell'agente di raccolta eventi di avvio

## <a name="purpose"></a>Scopo

Il provider WMI dell'agente di raccolta eventi di avvio fornisce l'accesso alle informazioni di connessione e configurazione per la funzionalità Raccolta eventi di installazione e avvio Windows Server. In questo modo è possibile visualizzare un elenco delle connessioni correnti e la cronologia delle connessioni tra un server dell'agente di raccolta e i relativi computer di destinazione. Inoltre, questo provider consente di gestire la configurazione di un server dell'agente di raccolta.

> [!Note]  
> Il provider WMI dell'agente di raccolta eventi di avvio viene implementato in BEvtCol.exe.

 

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Recupera i dati di inoltro da un computer di destinazione.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Destinazioni note contenenti i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

Cronologia recente delle modifiche apportate ai dati di inoltro per un computer di destinazione.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Controllo dell'istanza dell'agente di raccolta. Richiede i privilegi di amministratore (BA).

</dd> </dl>

 

 



