---
description: Per impostazione predefinita, il motore di ricerca e il catalogo di Windows non sono sensibili ai segni diacritici, ovvero i segni di accenti aggiunti alle lettere per modificare il significato o la pronuncia di una parola.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Riservatezza dei segni diacritici nelle ricerche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863684"
---
# <a name="diacritic-sensitivity-in-searches"></a>Riservatezza dei segni diacritici nelle ricerche

Per impostazione predefinita, il motore di ricerca e il catalogo di Windows non sono sensibili ai segni diacritici, ovvero i segni di accenti aggiunti alle lettere per modificare il significato o la pronuncia di una parola. Tuttavia, Windows ricerca consente di modificare questa impostazione per il catalogo usando [Gestione](-search-3x-wds-mngidx-catalog-manager.md) cataloghi per impostare la riservatezza dei segni diacritici. Ad esempio, con la distinzione dei segni diacritici impostata su **FALSE,** il catalogo considererebbe "resume" e "resumé" come se fossero la stessa parola.

A livello di query, i termini di query con segni diacritici nelle clausole FREETEXT e CONTAINS vengono passati al motore e quindi normalizzati (come in fase di indice) per la corrispondenza. La corrispondenza con il catalogo è sempre sensibile ai segni diacritici.

> [!Note]  
> Questo non è il caso per gli intervalli di caratteri 0x2e81-f8ff e 0x1100-0x11ff.

 

 

 



