---
description: Arresta il thread di risoluzione dei nomi utente.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Metodo DiskQuotaControl.ShutdownNameResolution (Dskquota.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da02f79ea8f7b582056e9c3c7c0c3f1db53fa9e08181559c99dd983924861c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459838"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Metodo DiskQuotaControl.ShutdownNameResolution

Arresta il thread di risoluzione dei nomi utente.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il sistema di risoluzione dei nomi dell'identificatore di sicurezza (SID) converte il SID in nomi utente in un thread in background. Questo thread viene arrestato automaticamente quando l'oggetto controllo quota associato viene eliminato. Tuttavia, in alcuni casi il thread non è più necessario, ma l'oggetto non è ancora pronto per l'eliminazione. Un esempio tipico è quando non è in corso alcuna ulteriore elaborazione, ma i client continuano a contenere riferimenti all'oggetto . Il **metodo ShutdownNameResolution** consente di terminare il thread del sistema di risoluzione e liberare le risorse associate senza eliminare l'oggetto di controllo della quota.

> [!Note]  
> Quando si arresta il thread del sistema di risoluzione, la risoluzione dei nomi asincrona si arresta immediatamente. Se successivamente vengono effettuate chiamate a metodi come [**AddUser**](diskquotacontrol-adduser.md) o [**FindUser,**](diskquotacontrol-finduser.md)l'oggetto quota potrebbe creare nuovamente il thread del sistema di risoluzione.

 

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

 

 




