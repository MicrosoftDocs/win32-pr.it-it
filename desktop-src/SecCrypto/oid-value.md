---
description: Imposta o Recupera il valore del numero punteggiato dell'OID dell'identificatore.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Proprietà Value
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
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333564"
---
# <a name="oidvalue-property"></a>OID. Proprietà Value

\[La proprietà **value** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **value** imposta o Recupera il valore del numero punteggiato dell'OID dell'identificatore.

## <a name="syntax"></a>Sintassi


```VB
OID.Value As String
```



## <a name="property-value"></a>Valore proprietà

Valore del numero punteggiato dell'OID dell'identificatore. Per i valori possibili, vedere Wincrypt. h.

## <a name="remarks"></a>Commenti

Se la proprietà **value** è impostata, la proprietà [**FriendlyName**](oid-friendlyname.md) viene impostata sul nome visualizzato corrispondente. Se la proprietà **FriendlyName** è impostata, la proprietà **value** viene impostata sul valore punteggiato corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
