---
title: Alberi di dominio
description: Un albero di dominio è costituito da diversi domini che condividono uno schema e una configurazione comuni, costituendo uno spazio dei nomi contiguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory albero di dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220949"
---
# <a name="domain-trees"></a>Alberi di dominio

Un *albero di dominio* è costituito da diversi domini che condividono uno schema e una configurazione comuni, costituendo uno spazio dei nomi contiguo. I domini in un albero sono collegati anche da relazioni di trust. Active Directory è un set di uno o più alberi.

Gli alberi possono essere visualizzati in due modi. Una vista rappresenta le relazioni di trust tra i domini. L'altra visualizzazione è lo spazio dei nomi dell'albero del dominio.

## <a name="viewing-trust-relationships"></a>Visualizzazione di relazioni di trust

È possibile creare un diagramma di un albero di dominio in base ai singoli domini e alla relazione di trust esistente.

Windows 2000 stabilisce relazioni di trust tra domini basati sul protocollo di sicurezza Kerberos. Il trust Kerberos è transitivo e gerarchico: se il dominio A considera attendibile il dominio B e il dominio B considera attendibile il dominio C, il dominio A considera attendibili il dominio C.

![relazione di trust albero di dominio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Visualizzazione dello spazio dei nomi

È anche possibile creare un diagramma di un albero di dominio basato sullo spazio dei nomi. È possibile determinare il nome distinto di un oggetto seguendo il percorso verso l'alto nella gerarchia dello spazio dei nomi dell'albero di dominio. Questa vista è utile per raggruppare gli oggetti in una gerarchia logica. Il vantaggio principale di uno spazio dei nomi contiguo è che una ricerca completa dalla radice dello spazio dei nomi Cerca nell'intera gerarchia.

![albero del dominio dello spazio dei nomi](images/namespace.png)

 

 




