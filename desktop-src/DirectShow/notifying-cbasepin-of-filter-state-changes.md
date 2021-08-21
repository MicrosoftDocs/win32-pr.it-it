---
description: Notifica a CBasePin delle modifiche dello stato del filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notifica a CBasePin delle modifiche dello stato del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152995"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notifica a CBasePin delle modifiche dello stato del filtro

La **classe CBasePin** viene notificata ogni volta che cambia lo stato del filtro proprietario. Per ogni transizione di stato, il filtro chiama un metodo corrispondente sul segnaposto, come illustrato nella tabella seguente.



| Nuovo stato filtro | Metodo CBasePin                                 |
|------------------|-------------------------------------------------|
| Arrestato          | [**CBasePin::Inactive**](cbasepin-inactive.md) |
| Paused           | [**CBasePin::Active**](cbasepin-active.md)     |
| In esecuzione          | [**CBasePin::Run**](cbasepin-run.md)           |



 

La classe derivata deve eseguire l'override di questi metodi per rispondere alla modifica dello stato. A seconda del filtro, il pin potrebbe avviare un thread di lavoro che fornisce campioni, esegue il commit o il decommit dell'allocatore di memoria e così via.

 

 



