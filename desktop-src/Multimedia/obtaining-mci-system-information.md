---
title: Recupero delle informazioni sul sistema MCI
description: Recupero delle informazioni sul sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Comando MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955372"
---
# <a name="obtaining-mci-system-information"></a>Recupero delle informazioni sul sistema MCI

Il comando [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) ottiene informazioni di sistema sui dispositivi MCI. MCI gestisce questo comando senza inoltrarlo a un dispositivo MCI. Per l'interfaccia del messaggio di comando, MCI restituisce le informazioni di sistema nella struttura [**\_ \_ parametri di MCI sysinfo**](mci-sysinfo-parms.md) .

È possibile usare il comando **sysinfo** (MCI \_ sysinfo) per recuperare informazioni come il numero di dispositivi MCI in un sistema, il numero di dispositivi MCI di un determinato tipo, il numero di dispositivi Open MCI e i nomi dei dispositivi. Questo comando viene spesso chiamato più di una volta per recuperare una particolare informazione. Ad esempio, è possibile recuperare il numero di dispositivi di un determinato tipo nella prima chiamata, quindi enumerare i nomi dei dispositivi nella successiva.

 

 




