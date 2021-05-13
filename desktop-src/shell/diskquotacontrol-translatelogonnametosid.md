---
description: Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.
title: Metodo DiskQuotaControl.TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841562"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Metodo DiskQuotaControl.TranslateLogonNameToSID

Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*logonname* 
</dt> <dd>

Tipo: **String**

Valore stringa che specifica il nome di accesso dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID di sicurezza utente (SID) in formato stringa corrispondente al nome di accesso specificato. La stringa restituita include le parentesi graffe di inclusione standard. Ad esempio:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Commenti

La stringa SID restituita può essere passata al [**metodo FindUser**](diskquotacontrol-finduser.md) al posto di un nome di accesso.

Quando una chiamata al metodo [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) ha esito negativo, potrebbe essere dovuta a una mancata corrispondenza tra il modulo (ad esempio, compatibile con SECURITY Account Manager SAM e l'UPN nome dell'entità utente ) del nome di accesso specificato e il modulo archiviato nella \[ cache \] \[ \] siD-name. In questi casi, il nome di accesso può essere convertito in un SID e la chiamata a **FindUser ripetuta.** **FindUser** riconosce una stringa SID e ignora la ricerca nella cache dei nomi SID. Il codice Microsoft Visual Basic Scripting Edition (VBScript) seguente illustra questa tecnica.


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



La conversione da nome a SID può essere un processo lento rispetto alle ricerche nella cache dei nomi SID. Pertanto, è consigliabile chiamare [**prima FindUser**](diskquotacontrol-finduser.md) con un nome di accesso. L'esempio precedente usa questa tecnica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




