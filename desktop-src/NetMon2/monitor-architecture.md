---
description: Nella figura seguente viene illustrata la relazione tra monitoraggi e altri componenti dell'architettura Network Monitor.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Architettura di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570681"
---
# <a name="monitor-architecture"></a>Architettura di monitoraggio

Nella figura seguente viene illustrata la relazione tra [*monitoraggi*](m.md) e altri componenti dell'architettura Network Monitor.

![relazione tra monitoraggi e altri componenti di Network Monitor](images/nmarch2.png)

Il traffico di rete viene raccolto (come singoli frame) dal driver NDIS. Il driver Network Monitor (Nmnt.sys) quindi instrada i frame a un provider di pacchetti di rete (NPP), che a sua volta acquisisce i dati in modalità in tempo reale. NPP è una raccolta di interfacce COM utilizzate per acquisire i dati. In questo caso, l'interfaccia [**IRTC**](irtc.md) viene utilizzata per eseguire un'acquisizione in tempo reale.

> [!Note]  
> L'oggetto NPP viene usato per le acquisizioni ritardate e in tempo reale. Per le acquisizioni ritardate utilizzate da esperti e parser, viene utilizzata l'interfaccia [**IDelaydC**](idelaydc.md) .

 

Il monitoraggio esamina quindi i dati acquisiti in modalità in tempo reale, individuando condizioni di rete specifiche e generando eventi in base alle esigenze.

Gli altri tre componenti vengono utilizzati dalle applicazioni di monitoraggio, ovvero lo strumento di controllo di monitoraggio, il servizio di controllo di monitoraggio (MCSVC) e l'Visualizzatore eventi:

-   Lo strumento di controllo di monitoraggio viene utilizzato per gestire le applicazioni di monitoraggio. Sono incluse la configurazione e l'esecuzione di tutte le applicazioni di monitoraggio.
-   Il servizio di controllo di monitoraggio (MCSVC) genera eventi, fornisce un collegamento di comunicazione a WMI per la visualizzazione degli eventi e coordina l'elaborazione delle operazioni di monitoraggio.
-   Il Visualizzatore eventi Visualizza gli eventi generati dal servizio di controllo di monitoraggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



