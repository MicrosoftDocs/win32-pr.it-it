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
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551309"
---
# <a name="csystemclock-class"></a>Classe CSystemClock

![gerarchia di classi csystemclock](images/sclock01.png)

La `CSystemClock` classe implementa un clock che restituisce l'ora di sistema.

Questa classe deriva dalla classe [**CBaseReferenceClock**](cbasereferenceclock.md) e aggiunge il supporto per le interfacce **IPersist** e [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .



| Metodi pubblici                                        | Descrizione                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Crea una nuova istanza di questo oggetto.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Metodo del costruttore.                                 |
| Metodi IAMClockAdjust                                | Descrizione                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Regola l'ora dell'orologio.                             |
| Metodi IPersist                                      | Descrizione                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Restituisce l'identificatore di classe (CLSID) dell'oggetto. |



 

 

 



