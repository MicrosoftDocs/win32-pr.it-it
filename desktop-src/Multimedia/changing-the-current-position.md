---
title: Modifica della posizione corrente
description: Modifica della posizione corrente
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14f062fc93a89f54fb89a30b6ac3e53c8d6240cfc28b661a25da48a0b1b2fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941289"
---
# <a name="changing-the-current-position"></a>Modifica della posizione corrente

Per modificare la posizione corrente in un elemento dispositivo, usare il messaggio di comando [**MCI \_ SEEK**](mci-seek.md) insieme al flag MCI TO e alla struttura \_ [**MCI \_ SEEK \_ PARMS.**](mci-seek-parms.md) Se si usa il **membro dwTo** per specificare una posizione di ricerca con MCI SEEK, è necessario eseguire una query sul formato dell'ora e impostarlo, \_ se necessario.

Oltre a specificare una posizione con il **membro dwTo,** è possibile specificare i flag MCI SEEK TO START o MCI SEEK TO END per il parametro dwParam1 della funzione \_ \_ \_ \_ \_ \_ [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))  per trovare le posizioni iniziale e finale dell'elemento dispositivo. Se si usa uno di questi flag, non specificare il flag MCI \_ TO.

 

 