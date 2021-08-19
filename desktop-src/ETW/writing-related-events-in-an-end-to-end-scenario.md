---
description: ETW consente di raggruppare gli eventi correlati da più componenti.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Scrittura di eventi correlati in uno scenario end-to-end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f1ddde6fa80c0ecd5f95373b6ba4d9b7fcf25e8b3e7be878b14830a404b1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813709"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Scrittura di eventi correlati in uno scenario end-to-end

ETW consente di raggruppare gli eventi correlati da più componenti. Ad esempio, se più componenti (nello stesso computer o in computer diversi) sono coinvolti nell'elaborazione degli stessi dati e ogni componente registra gli eventi per la relativa parte dell'attività, è possibile raggruppare tutti gli eventi correlati. Questo consentirà a un consumer di utilizzare tutti gli eventi, dall'inizio del processo alla fine del processo.

Per scrivere eventi correlati in un provider [basato su](about-event-tracing.md) manifesto, vedere Scrittura di eventi correlati in un provider basato [su manifesto](writing-related-events-in-a-manifest-base-provider.md).

Per scrivere eventi correlati in un provider [classico,](about-event-tracing.md) vedere [Scrittura di eventi correlati in un provider classico](tracing-event-instances.md).

 

 



