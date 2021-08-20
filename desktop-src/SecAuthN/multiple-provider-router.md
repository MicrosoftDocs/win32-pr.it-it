---
description: Il router a più provider gestisce la comunicazione tra il Windows operativo e i provider di rete installati. Consente Windows presentare una rete integrata all'utente.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Router con più provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786579"
---
# <a name="multiple-provider-router"></a>Router con più provider

Il [*router a più provider*](../secgloss/m-gly.md) gestisce la comunicazione tra il Windows operativo e i provider di rete installati. Consente Windows presentare una rete integrata all'utente.

All'avvio, la MPR controlla il Registro di sistema per determinare quali provider di rete sono installati nel sistema e l'ordine in cui devono essere eseguiti cicli. Carica tutte le DLL del provider di rete registrate e le usa per elaborare le chiamate WNet successive effettuate dall'interfaccia utente o da altre applicazioni.

Per altre informazioni sulle funzioni WNet, vedere Windows [Networking](../wnet/windows-networking-wnet-.md).

 

 
