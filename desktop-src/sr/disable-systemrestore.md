---
title: Metodo Disable della classe SystemRestore
description: Disabilita il monitoraggio in un'unità specifica.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Disabilitare il ripristino del sistema del metodo
- Disable System Restore Method, classe SystemRestore
- SystemRestore classe di ripristino di sistema, Disable (metodo)
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
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120026"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Metodo Disable della classe SystemRestore

Disabilita il monitoraggio in un'unità specifica.

## <a name="syntax"></a>Sintassi


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Unità* \[ di in\]
</dt> <dd>

Unità da disabilitare. Il formato della stringa dell'unità deve essere "C: \\ ". Se questo parametro è l'unità di sistema o una stringa vuota (""), non vengono monitorate unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK. In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | \\Impostazioni predefinite radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





