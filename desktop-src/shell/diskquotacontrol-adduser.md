---
description: Assegna una quota disco non predefinita a un nuovo utente.
title: Metodo DiskQuotaControl. AddUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525338"
---
# <a name="diskquotacontroladduser-method"></a>Metodo DiskQuotaControl. AddUser

Assegna una quota disco non predefinita a un nuovo utente.

## <a name="syntax"></a>Sintassi


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **char**

Valore stringa che contiene il nome di accesso dell'utente. Utilizzare la proprietà [**UserNameResolution**](diskquotacontrol-usernameresolution.md) per specificare la modalità di risoluzione del nome.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Object**

Restituisce un'espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.

## <a name="remarks"></a>Commenti

Il file system NTFS crea automaticamente una voce di quota utente quando un utente scrive per la prima volta nel volume. Alle voci create in questo modo vengono assegnati la soglia di avviso predefinita e i valori limite della quota hardware per il volume. Questo metodo consente di creare una voce di quota utente prima che un utente scriva le informazioni nel volume. Restituisce un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per assegnare una soglia di avviso o un valore di limite di quota diverso dalle impostazioni predefinite per il volume.

Se l'utente esiste già, non viene creata alcuna nuova voce. Il metodo restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) associato alla voce esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




