---
description: Per impostazione predefinita, il motore di ricerca di Windows e il catalogo non sono sensibili ai segni diacritici, che sono contrassegni accentati aggiunti alle lettere per modificare il significato o la pronuncia di una parola.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Distinzione tra segni diacritici nelle ricerche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306138"
---
# <a name="diacritic-sensitivity-in-searches"></a>Distinzione tra segni diacritici nelle ricerche

Per impostazione predefinita, il motore di ricerca di Windows e il catalogo non sono sensibili ai segni diacritici, che sono contrassegni accentati aggiunti alle lettere per modificare il significato o la pronuncia di una parola. Windows Search consente tuttavia di modificare questa impostazione per il catalogo usando [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) per impostare la sensibilità dei segni diacritici. Con la sensibilità dei segni diacritici impostata su **false**, ad esempio, il catalogo considera "Resume" e "curriculum" come se fossero la stessa parola.

A livello di query, i termini di query con segni diacritici nelle clausole FREETEXT e CONTAINs vengono passati al motore e vengono quindi normalizzati (come in fase di indicizzazione) per la corrispondenza. La corrispondenza con il catalogo è sempre sensibile ai segni diacritici.

> [!Note]  
> Questo non avviene per gli intervalli di caratteri 0x2e81-F8FF e 0x1100-0x11ff.

 

 

 



