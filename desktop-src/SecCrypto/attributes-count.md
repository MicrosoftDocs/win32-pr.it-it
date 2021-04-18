---
description: Recupera il numero di oggetti attributo nell'insieme.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Proprietà Attributes. Count
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
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329104"
---
# <a name="attributescount-property"></a>Proprietà Attributes. Count

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La proprietà **count** Recupera il numero di oggetti [**attribute**](attribute.md) nell'insieme.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di oggetti [**attributo**](attribute.md) nell'insieme. Ogni oggetto **attributo** rappresenta un singolo attributo nell'insieme.

## <a name="remarks"></a>Commenti

È possibile utilizzare la proprietà **count** per specificare l'ultimo oggetto [**attributo**](attribute.md) nella raccolta durante il recupero di un oggetto **attributo** specifico utilizzando la proprietà [**Attributes. Item**](attributes-item.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 
