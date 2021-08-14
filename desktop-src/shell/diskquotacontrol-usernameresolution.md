---
description: Imposta o ottiene un valore che controlla il modo in cui l'ID di sicurezza utente (SID) viene risolto in nomi utente.
title: DiskQuotaControl.UserNameResolution - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: cfc86f7f7da03ea4ffb092d50b51ef0c69349935cdae40586e08ae50f6ea251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224614"
---
# <a name="diskquotacontrolusernameresolution-property"></a>DiskQuotaControl.UserNameResolution - proprietà

Imposta o ottiene un valore che controlla il modo in cui l'ID di sicurezza utente (SID) viene risolto in nomi utente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà può essere impostata su uno dei valori seguenti.



| Tipo di risoluzione | Valore | Descrizione                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | Non risolvere le informazioni sul nome utente.                                                                                                                    |
| dqResolveSync   | 1     | Attendere durante la risoluzione delle informazioni sul nome.                                                                                                                   |
| dqResolveAsync  | 2     | Non attendere durante la risoluzione delle informazioni sul nome. [**L'evento OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) viene generato quando il nome viene risolto. |



 

## <a name="remarks"></a>Commenti

Questa proprietà influisce [**sull'enumerazione degli oggetti DIDiskQuotaUser**](didiskquotauser-object.md) e sui metodi [**AddUser**](diskquotacontrol-adduser.md) [**e FindUser.**](diskquotacontrol-finduser.md)

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

 

 




