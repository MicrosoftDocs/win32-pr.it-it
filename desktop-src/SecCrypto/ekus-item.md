---
description: Recupera l'oggetto EKU che rappresenta la proprietà EKU (Extended Key Usage) indicizzata.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: Proprietà IEKUs::Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b81e00de0ca8346d56ceafeb8b0d11353219c5fc6ab3eb0b29a9f7c868f79505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875151"
---
# <a name="iekusitem-property"></a>Proprietà IEKUs::Item

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Item** recupera l'oggetto [**EKU**](eku.md) che rappresenta la proprietà EKU (Extended Key Usage) indicizzata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**EKU**](eku.md) che rappresenta la proprietà EKU (Extended Key Usage) indicizzata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EKU**](ekus.md)
</dt> </dl>

 

 
