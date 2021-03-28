---
description: ETW fornisce un modo per raggruppare gli eventi correlati da più di un componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Scrittura di eventi correlati in uno scenario end-to-end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977767"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Scrittura di eventi correlati in uno scenario end-to-end

ETW fornisce un modo per raggruppare gli eventi correlati da più di un componente. Se, ad esempio, diversi componenti, nello stesso computer o in computer diversi, sono interessati all'elaborazione degli stessi dati e ogni componente registra gli eventi per la parte dell'attività, è possibile raggruppare tutti gli eventi correlati. Ciò consentirà a un consumer di utilizzare tutti gli eventi, dall'inizio del processo fino alla fine del processo.

Per scrivere eventi correlati in un provider [basato su manifesto](about-event-tracing.md) , vedere [scrittura di eventi correlati in un provider basato su manifesto](writing-related-events-in-a-manifest-base-provider.md).

Per scrivere eventi correlati in un provider [classico](about-event-tracing.md) , vedere [scrittura di eventi correlati in un provider classico](tracing-event-instances.md).

 

 



