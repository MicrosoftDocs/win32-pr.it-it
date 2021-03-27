---
description: Elimina un utente dal volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Metodo DiskQuotaControl. DeleteUser (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225920"
---
# <a name="diskquotacontroldeleteuser-method"></a>DiskQuotaControl. DeleteUser, metodo

Elimina un utente dal volume.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oUser (valore* 
</dt> <dd>

Tipo: **Object**

Espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo se l'utente è proprietario di una risorsa di archiviazione nel volume. Prima di eliminare un utente da un volume, è necessario eliminare tutte le archiviazioni per tale utente, spostarle in un altro volume o fare in modo che la sua proprietà venga trasferita a un altro utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




