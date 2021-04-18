---
description: Rappresenta le factory di attivazione registrate chiamando la funzione RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307063"
---
# <a name="ro_registration_cookie"></a>\_cookie di registrazione ro \_

Rappresenta le factory di attivazione registrate chiamando la funzione [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Commenti

La funzione [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) restituisce un **\_ \_ cookie di registrazione ro** quando un attivabile class factory viene registrato con la Windows Runtime. La funzione [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa il cookie per rimuovere le class factory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Roapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
