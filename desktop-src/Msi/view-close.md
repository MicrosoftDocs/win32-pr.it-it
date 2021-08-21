---
description: Il metodo Close dell'oggetto View termina l'esecuzione della query e rilascia le risorse del database.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Metodo View.Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: edbf2dd30902fa437fdd67d21efb86bb2edeabbd499f0f022501f166ad1b92a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498851"
---
# <a name="viewclose-method"></a>Metodo View.Close

Il **metodo Close** dell'oggetto [**View**](view-object.md) termina l'esecuzione della query e rilascia le risorse del database.

## <a name="syntax"></a>Sintassi


```JScript
View.Close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima che il [**metodo Execute**](view-execute.md) venga chiamato nuovamente nell'oggetto [**View,**](view-object.md) a meno che non siano state ottenute tutte le righe del set di risultati con il [**metodo Fetch.**](view-fetch.md) Viene chiamato internamente quando la vista viene distrutta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




