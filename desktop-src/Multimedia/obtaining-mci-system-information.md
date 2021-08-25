---
title: Ottenere l'System Information MCI
description: Ottenere l'System Information MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fa6cc0757bc09aa16216f2f20385bf31b44bb88e27ea64e091ff3909d8d57e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893221"
---
# <a name="obtaining-mci-system-information"></a>Ottenere l'System Information MCI

Il [comando sysinfo](sysinfo.md) ([**MCI \_ SYSINFO**](mci-sysinfo.md)) ottiene informazioni di sistema sui dispositivi MCI. MCI gestisce questo comando senza inoltrarlo a qualsiasi dispositivo MCI. Per l'interfaccia del messaggio di comando, MCI restituisce le informazioni di sistema nella [**struttura \_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

È possibile usare il comando **sysinfo** (MCI SYSINFO) per recuperare informazioni quali il numero di dispositivi MCI in un sistema, il numero di dispositivi MCI di un particolare tipo, il numero di dispositivi MCI aperti e i nomi dei \_ dispositivi. Questo comando viene spesso chiamato più volte per recuperare una particolare informazione. Ad esempio, è possibile recuperare il numero di dispositivi di un particolare tipo nella prima chiamata e quindi enumerare i nomi dei dispositivi nella successiva.

 

 




