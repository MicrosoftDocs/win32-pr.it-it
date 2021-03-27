---
description: Arresta il thread di risoluzione del nome utente.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Metodo DiskQuotaControl. ShutdownNameResolution (dskquota. h)
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
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049438"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>DiskQuotaControl. ShutdownNameResolution, metodo

Arresta il thread di risoluzione del nome utente.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il resolver di nomi SID (ID di sicurezza) converte il SID in nomi utente in un thread in background. Questo thread viene arrestato automaticamente quando l'oggetto di controllo della quota associato viene eliminato definitivamente. Tuttavia, esistono alcuni casi in cui il thread non è più necessario, ma l'oggetto non è ancora pronto per essere eliminato definitivamente. Un esempio tipico è quando non vengono eseguite altre elaborazioni, ma i client continuano a mantenere i riferimenti all'oggetto. Il metodo **ShutdownNameResolution** consente di terminare il thread del resolver e liberare le risorse associate senza eliminare definitivamente l'oggetto di controllo della quota.

> [!Note]  
> Quando si arresta il thread del resolver, la risoluzione dei nomi asincrona viene arrestata immediatamente. Se vengono successivamente effettuate chiamate a metodi quali [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md), l'oggetto quota potrebbe ricreare il thread del resolver.

 

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

 

 




