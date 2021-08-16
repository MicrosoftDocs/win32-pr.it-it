---
description: TAPI 2.0 offre un numero ridotto di miglioramenti alla funzionalità TAPI 1.4 di base.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926def5cf2348396b9197a83e17b35d9a91d4dee617e00abe4c02d0428f2884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861247"
---
# <a name="tapi-20"></a>TAPI 2.0

TAPI 2.0 offre un numero ridotto di miglioramenti alla funzionalità TAPI 1.4 di base. Tuttavia, sono state apportate alcune importanti modifiche all'architettura che ne hanno notevolmente migliorato la stabilità. La maggior parte delle modifiche sono state modifiche fondamentali necessarie per portare TAPI Windows NT 4.0 e sfruttarne le funzionalità (supporto completo a 32 bit, servizi e Unicode). Tuttavia, queste modifiche erano interne a TAPI e hanno avuto poco effetto sulle applicazioni TAPI.

Le applicazioni che supportano TAPI 1.3 e 1.4 (applicazioni a 16 bit tramite un livello di thunking) funzionano bene nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 e Windows NT. Tuttavia, l'effetto sugli sviluppatori di provider di servizi è stato significativo. I provider di servizi per questi sistemi operativi devono essere DLL Unicode completamente a 32 bit che possono essere eseguite nel contesto di TAPISRV, non nel contesto dell'applicazione TAPI (come hanno fatto tutti i TSP basati su Win16 precedenti). I TSP progettati per TAPI 1.4 non funzionano nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 o Windows NT.

TAPI 2.0 aggiunge anche le funzionalità importanti del supporto call center e del supporto QOS (Quality of Service).

I file binari di sistema TAPI Windows supportano TAPI versioni 1.3 e 1.4 per tutte le applicazioni. Tuttavia, le applicazioni a 16 bit non possono usare TAPI 2.0 e non è possibile usare un TSP TAPI 2.x a 16 bit.

 

 



