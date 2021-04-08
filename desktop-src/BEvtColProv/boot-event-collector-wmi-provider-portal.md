---
description: Il provider WMI raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità di raccolta degli eventi di avvio e di installazione in Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Provider WMI raccolta eventi di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877205"
---
# <a name="boot-event-collector-wmi-provider"></a>Provider WMI raccolta eventi di avvio

## <a name="purpose"></a>Scopo

Il provider WMI raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità di raccolta degli eventi di avvio e di installazione in Windows Server. In questo modo è possibile visualizzare un elenco delle connessioni correnti e la cronologia delle connessioni tra un server dell'agente di raccolta e i relativi computer di destinazione. Questo provider consente inoltre di gestire la configurazione di un server di raccolta.

> [!Note]  
> Il provider WMI di raccolta eventi di avvio viene implementato in BEvtCol.exe.

 

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Recupera i dati di invio da un computer di destinazione.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Destinazioni note che contengono i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

Cronologia recente delle modifiche apportate ai dati di invio per un computer di destinazione.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Controllo dell'istanza dell'agente di raccolta. Richiede i privilegi di amministratore (BA).

</dd> </dl>

 

 



