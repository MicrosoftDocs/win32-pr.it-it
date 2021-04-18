---
title: Metodo Enable della classe SystemRestore
description: Abilita il monitoraggio in un'unità specifica.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Abilita ripristino del sistema del metodo
- Enable Method System Restore, classe SystemRestore
- Ripristino del sistema della classe SystemRestore, metodo Enable
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301766"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Metodo Enable della classe SystemRestore

Abilita il monitoraggio in un'unità specifica.

## <a name="syntax"></a>Sintassi


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Unità* \[ di in\]
</dt> <dd>

Unità da abilitare. Il formato della stringa dell'unità deve essere "C: \\ ". Se questo parametro è l'unità di sistema o una stringa vuota (""), vengono monitorate tutte le unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK. In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.

## <a name="remarks"></a>Commenti

Il metodo **Enable** non attende che il monitoraggio venga abilitato completamente prima della restituzione, perché l'operazione potrebbe richiedere alcuni minuti. Viene invece restituito immediatamente dopo l'avvio del servizio Ripristino configurazione di sistema e del driver del filtro.

Per abilitare ripristino configurazione di sistema in un'unità non di sistema, è necessario innanzitutto abilitare ripristino configurazione di sistema nell'unità di sistema.

Questo metodo ha esito negativo in modalità provvisoria.

## <a name="examples"></a>Esempio


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
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

 

 





