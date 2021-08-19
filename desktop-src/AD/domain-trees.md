---
title: Alberi di dominio
description: Un albero di dominio è costituito da diversi domini che condividono uno schema e una configurazione comuni, formando uno spazio dei nomi contiguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- albero di dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a1e2ed05284d2a08735b048fb41d97d6597634f711094d0a3763c2d7f8be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430519"
---
# <a name="domain-trees"></a>Alberi di dominio

Un *albero di dominio* è costituito da diversi domini che condividono uno schema e una configurazione comuni, formando uno spazio dei nomi contiguo. Anche i domini in un albero sono collegati tra loro da relazioni di trust. Active Directory è un set di uno o più alberi.

Gli alberi possono essere visualizzati in due modi. Una visualizzazione è la relazione di trust tra domini. L'altra visualizzazione è lo spazio dei nomi dell'albero di dominio.

## <a name="viewing-trust-relationships"></a>Visualizzazione delle relazioni di trust

È possibile creare un diagramma di un albero di dominio basato sui singoli domini e sulla relazione di trust esistente.

Windows 2000 stabilisce relazioni di trust tra domini in base al protocollo di sicurezza Kerberos. Il trust Kerberos è transitivo e gerarchico: se il dominio A considera attendibile il dominio B e il dominio B considera attendibile il dominio C, il dominio A considera attendibile il dominio C.

![relazione di trust dell'albero di dominio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Visualizzazione dello spazio dei nomi

È anche possibile disegnare un diagramma di un albero di dominio basato sullo spazio dei nomi . È possibile determinare il nome distinto di un oggetto seguendo il percorso verso l'alto nella gerarchia dello spazio dei nomi dell'albero di dominio. Questa vista è utile per raggruppare gli oggetti in una gerarchia logica. Il vantaggio principale di uno spazio dei nomi contiguo è che una ricerca approfondita dalla radice dello spazio dei nomi esegue la ricerca nell'intera gerarchia.

![albero di dominio dello spazio dei nomi](images/namespace.png)

 

 




