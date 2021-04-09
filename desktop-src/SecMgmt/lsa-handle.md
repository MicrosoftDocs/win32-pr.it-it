---
description: Handle per l'oggetto Criteri locali.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050071"
---
# <a name="lsa_handle"></a>\_handle LSA

Il tipo di dati dell' **\_ handle LSA** è un handle per l'oggetto [**criterio**](policy-object.md) locale.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Commenti

Prima di poter usare l'API criteri locali, l'applicazione deve aprire un handle per un oggetto [**criteri**](policy-object.md) . A tale scopo, chiamare [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Questa funzione restituisce un handle che l'applicazione può quindi specificare nelle successive chiamate di funzione dei criteri LSA.

A ogni handle è associato un set di autorizzazioni che determina le operazioni che l'applicazione può eseguire sull'oggetto [**criterio**](policy-object.md) utilizzando l'handle. L'applicazione può aprire più di un handle per l'oggetto **criteri** alla volta. Quando un handle non è più necessario, l'applicazione deve chiuderla chiamando [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

