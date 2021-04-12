---
description: TAPI 2,0 fornisce un piccolo numero di miglioramenti alla funzionalità di base di TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345426"
---
# <a name="tapi-20"></a>TAPI 2,0

TAPI 2,0 fornisce un piccolo numero di miglioramenti alla funzionalità di base di TAPI 1,4. Tuttavia, sono state apportate alcune importanti modifiche architettoniche che hanno migliorato notevolmente la stabilità. La maggior parte delle modifiche sono state apportate modifiche fondamentali per l'uso di TAPI per Windows NT 4,0 e per sfruttare i vantaggi delle funzionalità (supporto completo a 32 bit, servizi e Unicode). Tuttavia, queste modifiche erano interne a TAPI e avevano un effetto minimo sulle applicazioni TAPI.

Le applicazioni che supportano TAPI 1,3 e 1,4 (applicazioni a 16 bit per mezzo di un livello di thunk) funzionano bene nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 e Windows NT. Tuttavia, l'effetto sugli sviluppatori del provider di servizi era significativo. I provider di servizi per questi sistemi operativi devono essere completamente dll Unicode a 32 bit che possono essere eseguite nel contesto di TAPISRV, non nel contesto dell'applicazione TAPI (come tutti i TSPs precedenti basati su Win16). TSPs progettato per TAPI 1,4 non funziona nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 o Windows NT.

TAPI 2,0 aggiunge inoltre le funzionalità importanti del supporto del Call Center e del supporto di qualità del servizio (QOS).

I file binari di sistema TAPI disponibili in Windows supportano le versioni di TAPI 1,3 e 1,4 per tutte le applicazioni. Tuttavia, le applicazioni a 16 bit non possono usare TAPI 2,0 e non è possibile usare un TSP a 16 bit TAPI 2. x.

 

 



