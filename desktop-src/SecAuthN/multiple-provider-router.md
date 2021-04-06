---
description: Il router multi-provider (MPR) gestisce la comunicazione tra il sistema operativo Windows e i provider di rete installati. Consente a Windows di presentare una rete integrata all'utente.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Router per più provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883890"
---
# <a name="multiple-provider-router"></a>Router per più provider

Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) gestisce la comunicazione tra il sistema operativo Windows e i provider di rete installati. Consente a Windows di presentare una rete integrata all'utente.

All'avvio di MPR, viene controllato il registro di sistema per determinare quali provider di rete sono installati nel sistema e l'ordine in cui devono essere ciclati. Carica tutte le dll del provider di rete registrate e le usa per elaborare le chiamate WNet successive effettuate dall'interfaccia utente o da altre applicazioni.

Per ulteriori informazioni sulle funzioni WNet, vedere la pagina relativa alla [rete Windows](../wnet/windows-networking-wnet-.md).

 

 
