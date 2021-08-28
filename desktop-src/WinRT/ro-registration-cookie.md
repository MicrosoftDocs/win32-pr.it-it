---
description: Rappresenta le factory di attivazione registrate chiamando la funzione RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741598"
---
# <a name="ro_registration_cookie"></a>COOKIE \_ DI REGISTRAZIONE \_ RO

Rappresenta le factory di attivazione registrate chiamando la [**funzione RoRegisterActivationFactories.**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Commenti

La [**funzione RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) restituisce un **\_ \_ COOKIE** DI REGISTRAZIONE RO quando una class factory attivabile viene registrata con Windows Runtime. La [**funzione RoRevokeActivationFactories usa**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) il cookie per rimuovere le class factory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Roapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
