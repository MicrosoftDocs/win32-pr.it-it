---
description: Imposta o Recupera il nome visualizzato per l'identificatore.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. Proprietà FriendlyName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332009"
---
# <a name="oidfriendlyname-property"></a>OID. Proprietà FriendlyName

\[La proprietà **FriendlyName** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **FriendlyName** imposta o Recupera il nome visualizzato per l'identificatore.

## <a name="syntax"></a>Sintassi


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Valore proprietà

Nome visualizzato per l' [**OID**](oid.md).

## <a name="remarks"></a>Commenti

Se la proprietà **FriendlyName** è impostata, la proprietà [**value**](oid-value.md) viene impostata sul valore punteggiato corrispondente. Se la proprietà **value** è impostata, la proprietà **FriendlyName** viene impostata sul nome visualizzato corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
