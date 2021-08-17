---
description: Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione select era il mezzo standard (e solo) per ottenere le indicazioni degli eventi di rete.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Seleziona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740923"
---
# <a name="selects"></a>Seleziona

Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era il mezzo standard (e solo) per ottenere le indicazioni degli eventi di rete. Per ogni socket, è possibile eseguire il polling o attendere le informazioni sullo stato di lettura, scrittura o errore. Per [**altre informazioni, vedere WSPSelect.**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) Si noti che la QOS FD dell'evento di \_ rete non può essere ottenuta con questo approccio.

 

 
