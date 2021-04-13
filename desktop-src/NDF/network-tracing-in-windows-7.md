---
title: Traccia di rete in Windows 7
description: Windows 7 si espande sul Framework di diagnostica di rete (NDF) per fornire un metodo rapido per la risoluzione dei problemi di connettività di rete abilitando la raccolta di tutte le informazioni necessarie in un unico passaggio e sfruttando Event Tracing for Windows (ETW) per registrare i pacchetti di eventi di rete in un unico file.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399693"
---
# <a name="network-tracing-in-windows-7"></a>Traccia di rete in Windows 7

Con l'aumentare della complessità dello stack di rete, è spesso difficile tracciare e diagnosticare rapidamente i problemi all'interno dello stack. Windows 7 si espande sul Framework di diagnostica di rete (NDF) per fornire un metodo rapido per la risoluzione dei problemi di connettività di rete abilitando la raccolta di tutte le informazioni necessarie in un unico passaggio e sfruttando [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per registrare gli eventi di rete & pacchetti in un unico file.

Gli eventi e i pacchetti correlati vengono raggruppati per una determinata attività, ad esempio l'esplorazione di un sito Web, tra i vari componenti nello stack di rete. L'output di questo processo è un file di log di traccia eventi (ETL). Consentendo la visualizzazione di tutti gli eventi correlati a un'attività specifica in una sola volta in questo file, è possibile ridurre notevolmente il tempo necessario per isolare e diagnosticare i problemi di rete.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [Traccia di rete in Windows 7: architettura](network-tracing-in-windows-7-architecture.md)                                |
| [Strumenti per la risoluzione dei problemi tramite la traccia di rete in Windows 7](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [Traccia di rete in Windows 7: scenari](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 