---
title: Metodo Disable della classe SystemRestore
description: Disabilita il monitoraggio in una determinata unità.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Disabilitare l'Ripristino configurazione di sistema
- Disabilitare il Ripristino configurazione di sistema , classe SystemRestore
- Metodo Disable Ripristino configurazione di sistema classe SystemRestore
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a05d53ee13e2f06c2f4765d2947f49a417ed798965406185619dfce207cf76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452922"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Metodo Disable della classe SystemRestore

Disabilita il monitoraggio in una determinata unità.

## <a name="syntax"></a>Sintassi


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Unità* \[ Pollici\]
</dt> <dd>

Unità da disabilitato. La stringa di unità deve essere nel formato \\ "C:". Se questo parametro è l'unità di sistema o una stringa vuota (""), non viene monitorata alcuna unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S \_ OK. In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError.h.

## <a name="examples"></a>Esempio


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | Impostazione \\ predefinita radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





