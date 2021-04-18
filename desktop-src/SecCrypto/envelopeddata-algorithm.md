---
description: Recupera l'algoritmo di crittografia e la lunghezza della chiave.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: Proprietà EnvelopedData. Algorithm
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
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327899"
---
# <a name="envelopeddataalgorithm-property"></a>Proprietà EnvelopedData. Algorithm

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Algorithm** recupera l'algoritmo di crittografia e la [*lunghezza della chiave*](../secgloss/k-gly.md).

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**algoritmo**](algorithm.md) che contiene l'algoritmo di crittografia e la lunghezza della chiave.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
