---
description: Invalida la cache dei nomi utente dell'ID di sicurezza.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Metodo DiskQuotaControl.InvalidateSidNameCache (Dskquota.h)
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
ms.openlocfilehash: 1a171aaaf8f3faa45f967f29bf0f9d742aa0fe0221b46ae4ba4f8527d9cf9715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455891"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Metodo DiskQuotaControl.InvalidateSidNameCache

Invalida la cache dei nomi utente dell'ID di sicurezza.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I nomi utente e gli ID di sicurezza associati vengono archiviati in una cache. È possibile cancellare questa cache chiamando **InvalidateSidNameCache**. Se successivamente si crea un nuovo oggetto utente, le informazioni devono essere ottenute dal controller di dominio e la cache dovrà essere ristabilita.

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

 

 




