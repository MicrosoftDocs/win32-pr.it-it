---
description: Si verifica quando sono state risolte le informazioni sul nome per un oggetto DIDiskQuotaUser.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Funzione OnUserNameChanged (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346436"
---
# <a name="onusernamechanged-function"></a>OnUserNameChanged (funzione)

Si verifica quando sono state risolte le informazioni sul nome per un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*oUser (valore* 
</dt> <dd>

**Oggetto** che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) associato all'utente il cui nome è stato risolto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un client [**enumera gli utenti**](didiskquotauser-object.md)o chiama il metodo [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md) , il nome utente deve essere risolto nell'ID di sicurezza (SID) associato. Poiché questa procedura può richiedere molto tempo, un client può avere la risoluzione dei nomi eseguita in modo asincrono in un thread in background. Quando il nome di un utente viene risolto, l'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) invia una notifica al client generando l'evento **OnUserNameChanged** . Un oggetto **DIDiskQuotaUser** associato all'utente viene passato come parametro. Questo oggetto consente al client di modificare le impostazioni di quota dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




