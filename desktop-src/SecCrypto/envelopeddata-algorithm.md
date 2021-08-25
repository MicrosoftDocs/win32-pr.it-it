---
description: Recupera l'algoritmo di crittografia e la lunghezza della chiave.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData.Algorithm - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58971f27c271e18cef63f670a74ad0b78bbcb92914d35d9c6ca1f8461dfe15ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874411"
---
# <a name="envelopeddataalgorithm-property"></a>EnvelopedData.Algorithm - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Algorithm** recupera l'algoritmo di crittografia e la lunghezza della [*chiave*](../secgloss/k-gly.md).

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Algorithm**](algorithm.md) che contiene l'algoritmo di crittografia e la lunghezza della chiave.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
