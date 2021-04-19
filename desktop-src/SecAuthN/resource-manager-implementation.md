---
description: Resource Manager viene eseguito come servizio attendibile in un singolo processo. Tutte le richieste per l'accesso tramite smart card vengono effettuate al gestore di risorse, che le instrada al lettore che contiene la scheda di destinazione.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implementazione di Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311611"
---
# <a name="resource-manager-implementation"></a>Implementazione di Gestione risorse

[*Resource Manager*](../secgloss/r-gly.md) viene eseguito come servizio attendibile in un singolo processo. Tutte le richieste per l'accesso tramite [*Smart Card*](../secgloss/s-gly.md) vengono effettuate al gestore di risorse, che le instrada al [*lettore*](../secgloss/r-gly.md) che contiene la scheda di destinazione.

Le smart card vengono spesso utilizzate in combinazione con sicurezza e privacy personali. Laddove possibile, Resource Manager usa i meccanismi di sicurezza esistenti all'interno del sistema operativo sottostante durante l'accesso a un lettore o a una smart card.

 

 
