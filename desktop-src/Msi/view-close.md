---
description: Il metodo Close dell'oggetto View termina l'esecuzione della query e rilascia le risorse di database.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close (metodo)
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
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328754"
---
# <a name="viewclose-method"></a>View. Close (metodo)

Il metodo **Close** dell'oggetto [**View**](view-object.md) termina l'esecuzione della query e rilascia le risorse di database.

## <a name="syntax"></a>Sintassi


```JScript
View.Close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima che il metodo [**Execute**](view-execute.md) venga chiamato nuovamente sull'oggetto [**View**](view-object.md) , a meno che tutte le righe del set di risultati non siano state ottenute con il metodo [**Fetch**](view-fetch.md) . Viene chiamato internamente quando la vista viene distrutta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




