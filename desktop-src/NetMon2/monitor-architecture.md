---
description: Nella figura seguente viene illustrata la relazione tra monitoraggi e altri componenti dell'Network Monitor architettura.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Monitorare l'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cd0a099fc1474255b36f1f04d28899b25a527fee19ba1d29434b4692615ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677127"
---
# <a name="monitor-architecture"></a>Monitorare l'architettura

Nella figura seguente viene illustrata la relazione [*tra monitoraggi*](m.md) e altri componenti dell Network Monitor architettura.

![relazione tra monitoraggi e altri componenti di Network Monitor](images/nmarch2.png)

Il traffico di rete viene raccolto (come singoli frame) dal driver NDIS. Il Network Monitor driver (Nmnt.sys) instrada quindi i frame a un provider di pacchetti di rete (NPP), che a sua volta acquisisce i dati in modalità in tempo reale. NPP è una raccolta di interfacce COM usate per acquisire i dati. In questo caso, [**l'interfaccia IRTC**](irtc.md) viene usata per eseguire un'acquisizione in tempo reale.

> [!Note]  
> NPP viene usato per le acquisizioni in tempo reale e in ritardo. Per le acquisizioni ritardate usate da esperti e parser, viene usata l'interfaccia [**IDelaydC.**](idelaydc.md)

 

Il monitoraggio esamina quindi i dati acquisiti in modalità in tempo reale, rilevando condizioni di rete specifiche e generando eventi in base alle esigenze.

Altri tre componenti vengono usati dalle applicazioni di monitoraggio: strumento di controllo monitoraggio, servizio di controllo di monitoraggio (MCSVC) e Visualizzatore eventi:

-   Lo strumento di controllo monitoraggio viene usato per gestire le applicazioni di monitoraggio. Ciò include la configurazione e l'esecuzione di tutte le applicazioni di monitoraggio.
-   Il servizio di controllo di monitoraggio (MCSVC) genera eventi, fornisce un collegamento di comunicazione a WMI per la visualizzazione degli eventi e coordina l'elaborazione delle operazioni di monitoraggio.
-   Il Visualizzatore eventi visualizza gli eventi generati dal servizio di controllo di monitoraggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Imonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



