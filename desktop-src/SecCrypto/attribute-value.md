---
description: Imposta o recupera il valore dell'attributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Proprietà Attribute.Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773705"
---
# <a name="attributevalue-property"></a>Proprietà Attribute.Value

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/previous-versions/windows/)\]

La **proprietà Value** imposta o recupera il valore dell'attributo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Valore proprietà

Variabile **Variant** che contiene il valore dell'attributo. Per **gli attributi \_ CAPICOM AUTHENTICATED \_ ATTRIBUTE SIGNING \_ \_ TIME,** il tipo di dati è **DATE**. Per tutti gli altri attributi, il valore della proprietà è una stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
