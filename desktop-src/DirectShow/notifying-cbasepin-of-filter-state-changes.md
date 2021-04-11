---
description: Notifica di CBasePin delle modifiche allo stato del filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notifica di CBasePin delle modifiche allo stato del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341751"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notifica di CBasePin delle modifiche allo stato del filtro

La classe **CBasePin** riceve una notifica ogni volta che lo stato del filtro proprietario viene modificato. Per ogni transizione di stato, il filtro chiama un metodo corrispondente sul pin, come illustrato nella tabella seguente.



| Nuovo stato filtro | Metodo CBasePin                                 |
|------------------|-------------------------------------------------|
| Arrestato          | [**CBasePin:: inactive**](cbasepin-inactive.md) |
| Paused           | [**CBasePin:: Active**](cbasepin-active.md)     |
| In esecuzione          | [**CBasePin:: Run**](cbasepin-run.md)           |



 

La classe derivata deve eseguire l'override di questi metodi per rispondere alla modifica dello stato. A seconda del filtro, il PIN potrebbe avviare un thread di lavoro che fornisce esempi, eseguire il commit o il decommit dell'allocatore di memoria e così via.

 

 



