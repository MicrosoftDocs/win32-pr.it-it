---
description: Invalida la cache del nome utente dell'ID di sicurezza.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Metodo DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966521"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>DiskQuotaControl. InvalidateSidNameCache, metodo

Invalida la cache del nome utente dell'ID di sicurezza.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I nomi utente e gli ID di sicurezza associati vengono archiviati in una cache. È possibile cancellare la cache chiamando **InvalidateSidNameCache**. Se successivamente si crea un nuovo oggetto utente, le informazioni dovranno essere ottenute dal controller di dominio e sarà necessario ristabilire la cache.

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

 

 




