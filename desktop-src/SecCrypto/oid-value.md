---
description: Imposta o recupera il valore del numero OID punteggiato dell'identificatore.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: Oid. Proprietà Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: edaca987dbba57127c922161fbc6c6cd9473732ba1b7d1339618009335c904cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979733"
---
# <a name="oidvalue-property"></a>Oid. Proprietà Value

\[La **proprietà Value** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe Oid nello**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Value** imposta o recupera il valore del numero OID punteggiato dell'identificatore.

## <a name="syntax"></a>Sintassi


```VB
OID.Value As String
```



## <a name="property-value"></a>Valore proprietà

Valore del numero OID punteggiato dell'identificatore. Per i valori possibili, vedere Wincrypt.h.

## <a name="remarks"></a>Commenti

Se la **proprietà Value** è impostata, la [**proprietà FriendlyName**](oid-friendlyname.md) viene impostata sul nome visualizzato corrispondente. Se la **proprietà FriendlyName** è impostata, la **proprietà Value** viene impostata sul valore punteggiato corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oid**](oid.md)
</dt> </dl>

 

 
