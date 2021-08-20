---
description: Si verifica quando le informazioni sul nome per un oggetto DIDiskQuotaUser sono state risolte.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Funzione OnUserNameChanged (Dskquota.h)
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
ms.openlocfilehash: 02e4227e06d9c9303a5fe9b799afff6e452843bbb7c0dac096b39f925e568d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459894"
---
# <a name="onusernamechanged-function"></a>Funzione OnUserNameChanged

Si verifica quando le informazioni sul nome [**per un oggetto DIDiskQuotaUser**](didiskquotauser-object.md) sono state risolte.

## <a name="parameters"></a>Parametri

<dl> <dt>

*oUser* 
</dt> <dd>

Oggetto **che** restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) associato all'utente il cui nome è stato risolto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un client [**enumera gli utenti**](didiskquotauser-object.md)o chiama il metodo [**AddUser**](diskquotacontrol-adduser.md) o [**FindUser,**](diskquotacontrol-finduser.md) il nome utente deve essere risolto nell'ID di sicurezza (SID) associato. Poiché questa procedura può richiedere molto tempo, la risoluzione dei nomi di un client può essere eseguita in modo asincrono in un thread in background. Quando il nome di un utente viene risolto, l'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) invia una notifica al client generando **l'evento OnUserNameChanged.** Un **oggetto DIDiskQuotaUser** associato all'utente viene passato come parametro. Questo oggetto consente al client di modificare le impostazioni di quota dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




