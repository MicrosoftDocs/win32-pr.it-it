---
description: Il metodo GetError dell'oggetto View restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Metodo View.GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038801"
---
# <a name="viewgeterror-method"></a>Metodo View.GetError

Il **metodo GetError** dell'oggetto [**View**](view-object.md) restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore. Nell'automazione il valore restituito è una stringa nel formato ColumnName, dove rappresenta un codice di errore \# \# \# \# a 2 cifre. Restituisce il primo errore nella matrice di errori della vista. Le chiamate successive restituiscono il valore successivo nella matrice di errori. Quando viene restituito il valore "00", non esistono altri errori e le chiamate successive semplicemente esercitere un nuovo ciclo nella matrice.

## <a name="syntax"></a>Sintassi


```JScript
View.GetError()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView è definito come \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




