---
title: Metodo GetLastRestoreStatus della classe SystemRestore
description: Recupera lo stato dell'ultimo ripristino di sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Ripristino del sistema del metodo GetLastRestoreStatus
- Ripristino del sistema del metodo GetLastRestoreStatus, classe SystemRestore
- SystemRestore Class System Restore, metodo GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300978"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Metodo GetLastRestoreStatus della classe SystemRestore

Recupera lo stato dell'ultimo ripristino di sistema.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori di stato seguenti.



| Valore restituito                                                                 | Descrizione                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'ultimo ripristino non è riuscito.<br/>          |
| <dl> <dt>1</dt> </dl> | L'ultimo ripristino è stato completato correttamente.<br/>  |
| <dl> <dt>2</dt> </dl> | L'ultimo ripristino è stato interrotto.<br/> |



 

## <a name="examples"></a>Esempio


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
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

 

 





