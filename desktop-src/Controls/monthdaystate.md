---
title: MONTHDAYSTATE
description: Il tipo di dati MONTHDAYSTATE è un bit che include lo stato di ogni giorno di un mese.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855498"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Il tipo di dati MONTHDAYSTATE è un bit che include lo stato di ogni giorno di un mese. Il tipo di dati è definito in commctrl. h come segue:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Ogni bit (da 0 a 30) rappresenta lo stato di un giorno in un mese. Se un bit è acceso, il giorno corrispondente verrà visualizzato in grassetto. in caso contrario, verrà visualizzato senza enfasi.

Questo tipo di dati viene usato con il messaggio [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) e con la macro corrispondente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Quando i valori di MONTHDAYSTATE vengono utilizzati in riferimento a mesi inferiori a 31 giorni, sarà possibile accedere solo ai bit necessari.

Questo tipo di dati è stato definito per la prima volta nella [versione 4,70](common-control-versions.md) del Comctl32.dll.

 

 




