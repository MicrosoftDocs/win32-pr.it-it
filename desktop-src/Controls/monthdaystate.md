---
title: MONTHDAYSTATE
description: Il tipo di dati MONTHDAYSTATE è un campo di bit che contiene lo stato di ogni giorno in un mese.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079861"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Il tipo di dati MONTHDAYSTATE è un campo di bit che contiene lo stato di ogni giorno in un mese. Il tipo di dati è definito in Commctrl.h come indicato di seguito:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Ogni bit (da 0 a 30) rappresenta lo stato di un giorno in un mese. Se un bit è on, il giorno corrispondente verrà visualizzato in grassetto. In caso contrario, verrà visualizzato senza enfasi.

Questo tipo di dati viene usato con il [**messaggio \_ MCM SETDAYSTATE**](mcm-setdaystate.md) e la macro corrispondente, [**MonthCal \_ SetDayState.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) Quando i valori MONTHDAYSTATE vengono usati in riferimento a mesi più brevi di 31 giorni, sarà possibile accedere solo ai bit necessari.

Questo tipo di dati è stato definito per [la prima volta nella versione 4.70](common-control-versions.md) di Comctl32.dll.

 

 




