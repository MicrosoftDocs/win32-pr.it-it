---
description: L'enumerazione CAPICOM \_ KEY STORAGE FLAG definisce i flag di archiviazione delle \_ \_ chiavi.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: CAPICOM_KEY_STORAGE_FLAG enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cb1c2c4761403223c8ed0eb225709fbd189127bc9d56d60b82a534e2bc15b8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879091"
---
# <a name="capicom_key_storage_flag-enumeration"></a>Enumerazione CAPICOM \_ KEY \_ STORAGE \_ FLAG

**L'enumerazione CAPICOM \_ KEY STORAGE \_ \_ FLAG** definisce i flag di archiviazione delle chiavi.

## <a name="members"></a>Membri



| Membro                                     | Descrizione                           | Valore |
|--------------------------------------------|---------------------------------------|-------|
| **IMPOSTAZIONE PREDEFINITA \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM**         | Archiviazione chiavi predefinita.<br/>       | 0     |
| **ARCHIVIAZIONE CHIAVI CAPICOM \_ \_ \_ ESPORTABILE**      | La chiave è esportabile.<br/>     | 1     |
| **PROTEZIONE \_ DELL'UTENTE \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM** | La chiave è protetta dall'utente.<br/> | 2     |



## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dal metodo seguente:

-   [**Certificate.Load**](certificate-load.md)
-   [**Store.Load**](store-load.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




