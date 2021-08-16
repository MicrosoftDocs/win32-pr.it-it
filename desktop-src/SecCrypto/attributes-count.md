---
description: Recupera il numero di oggetti Attribute nella raccolta.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes.Count - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d7b1f2213fc6de3ec08a9c9b568222f5dd54a6de6f9bdb3adb27e052e8c088e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773506"
---
# <a name="attributescount-property"></a>Attributes.Count - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la classe [**CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/previous-versions/windows/)\]

La **proprietà Count** recupera il numero di oggetti [**Attribute**](attribute.md) nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di [**oggetti Attribute**](attribute.md) nella raccolta. Ogni **oggetto Attribute** rappresenta un singolo attributo nella raccolta.

## <a name="remarks"></a>Commenti

La **proprietà Count** può essere usata per specificare l'ultimo oggetto [**Attribute**](attribute.md) nella raccolta quando si recupera un oggetto **Attribute** specifico usando la [**proprietà Attributes.Item.**](attributes-item.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 
