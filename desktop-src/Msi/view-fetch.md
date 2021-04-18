---
description: Il metodo fetch dell'oggetto View recupera la riga successiva di dati della colonna se nel set di risultati sono disponibili più righe. in caso contrario, è null. Chiamare il metodo Execute prima del metodo fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. fetch (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324766"
---
# <a name="viewfetch-method"></a>View. fetch (metodo)

Il metodo **Fetch** dell'oggetto [**View**](view-object.md) recupera la riga successiva di dati della colonna se nel set di risultati sono disponibili più righe. in caso contrario, è null. Chiamare il metodo [**Execute**](view-execute.md) prima del metodo **Fetch** .

## <a name="syntax"></a>Sintassi


```JScript
View.Fetch()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È necessario utilizzare lo stesso oggetto [**record**](record-object.md) per recuperare i dati in più righe. in caso contrario, l'oggetto deve essere rilasciato uscendo dall'ambito. Il record può essere testato per la fine del set di risultati utilizzando la sintassi "If FetchRecord is Nothing".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




