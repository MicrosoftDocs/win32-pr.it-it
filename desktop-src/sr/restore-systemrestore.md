---
title: Metodo Restore della classe SystemRestore
description: Avvia un ripristino di sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Ripristino del sistema del metodo Restore
- Ripristino del sistema del metodo Restore, classe SystemRestore
- SystemRestore classe di ripristino del sistema, metodo Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740311"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Metodo Restore della classe SystemRestore

Avvia un ripristino di sistema. Il chiamante deve forzare il riavvio del sistema. Il ripristino effettivo si verifica durante il riavvio.

## <a name="syntax"></a>Sintassi


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SequenceNumber* \[ in\]
</dt> <dd>

Numero di sequenza del punto di ripristino. Per determinare il numero di sequenza di un punto di ripristino specifico, enumerare tutti i punti di ripristino nel sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK. In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.

## <a name="examples"></a>Esempio


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                         |
| Spazio dei nomi<br/>                | \\ \\ Impostazioni predefinite radice<br/>                                                        |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





