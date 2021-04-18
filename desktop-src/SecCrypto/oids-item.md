---
description: Recupera un oggetto OID dalla raccolta. Si tratta della proprietà predefinita.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: Proprietà Oid. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325159"
---
# <a name="oidsitem-property"></a>Proprietà Oid. Item

\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Item** recupera un oggetto [**OID**](oid.md) dalla raccolta. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) in corrispondenza dell'indice specificato o dell'oggetto **OID** con il valore tratteggiato specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
