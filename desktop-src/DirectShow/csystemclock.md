---
description: La classe CSystemClock implementa un clock che restituisce l'ora di sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Classe CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: c608b1d3f44a82d7aa964e803dec147a7216a71e85c6d797135713cf28af3fa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317226"
---
# <a name="csystemclock-class"></a>Classe CSystemClock

![Gerarchia di classi csystemclock](images/sclock01.png)

La `CSystemClock` classe implementa un clock che restituisce l'ora di sistema.

Questa classe deriva dalla [**classe CBaseReferenceClock**](cbasereferenceclock.md) e aggiunge il supporto per le **interfacce IPersist** e [**IAMClockAdjust.**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)



| Metodi pubblici                                        | Descrizione                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Crea una nuova istanza di questo oggetto.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Metodo del costruttore.                                 |
| Metodi IAMClockAdjust                                | Descrizione                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Regola l'ora dell'orologio.                             |
| Metodi IPersist                                      | Descrizione                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Restituisce l'identificatore di classe (CLSID) dell'oggetto. |



 

 

 



