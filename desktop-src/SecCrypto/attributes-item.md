---
description: Recupera l'oggetto Attribute che rappresenta l'attributo indicizzato.
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Proprietà Attributes.Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 94f1ab0f9e2ef48892b27ddc51d3ac3fd1a61216d63bf4a81013e7565710a1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879831"
---
# <a name="attributesitem-property"></a>Proprietà Attributes.Item

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Item** recupera l'oggetto [**Attribute**](attribute.md) che rappresenta l'attributo indicizzato. Si tratta della proprietà predefinita.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Attribute**](attribute.md) che rappresenta l'attributo indicizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
