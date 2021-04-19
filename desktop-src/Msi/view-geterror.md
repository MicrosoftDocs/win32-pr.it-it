---
description: Il metodo getError dell'oggetto View restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError, metodo
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
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326535"
---
# <a name="viewgeterror-method"></a>View. GetError, metodo

Il metodo **GetError** dell'oggetto [**View**](view-object.md) restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore. In automazione, il valore restituito è una stringa nel formato \# \# ColumnName, dove \# \# rappresenta un codice di errore a 2 cifre. Restituisce il primo errore nella matrice di errori della visualizzazione. le chiamate successive restituiscono il valore successivo nella matrice di errori. Quando viene restituito il valore '00 ', non sono presenti altri errori e le chiamate successive passano di nuovo a scorrere la matrice.

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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




