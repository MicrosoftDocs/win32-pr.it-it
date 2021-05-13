---
description: Trova la voce di un utente, in base al nome, nel file di quota del volume.
title: Metodo DiskQuotaControl.FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841522"
---
# <a name="diskquotacontrolfinduser-method"></a>Metodo DiskQuotaControl.FindUser

Trova la voce di un utente, in base al nome, nel file di quota del volume.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **String**

Valore stringa che contiene il nome di accesso dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un'espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser dell'utente.**](didiskquotauser-object.md)

## <a name="remarks"></a>Commenti

Questo metodo restituisce un [**oggetto DIDiskQuotaUser**](didiskquotauser-object.md) anche se non è presente alcuna voce per l'utente nel file di quota. L'oggetto utente restituito ha una soglia di avviso e limiti di quota rigida impostati su valori predefiniti del volume.

La stringa restituita [**da TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) può essere passata al posto del *parametro sLogonName.* Quando **FindUser** riceve una stringa SID, usa il SID corrispondente per la ricerca diretta del record di quota dell'utente nel volume. In questo modo viene ignorata la cache dei nomi SID. Nei casi in cui **FindUser** ha esito negativo a causa di una mancata corrispondenza nel formato (ad esempio, compatibile con SAM e UPN) del nome di accesso specificato e del nome di accesso memorizzato nella cache, il nome di accesso può essere convertito in una stringa SID usando **TranslateLogonNameToSID** e quindi passato nuovamente a **FindUser**. Il codice VBScript seguente illustra questa tecnica.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




