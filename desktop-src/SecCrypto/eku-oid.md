---
description: Imposta o recupera una stringa che contiene un valore stringa OID EKU come definito in Wincrypt.h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: Proprietà IEKU::OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 49a35cb223c338573ba0a52288a1e5528820dcbd4c7589548ce31f9df46dc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875251"
---
# <a name="iekuoid-property"></a>Proprietà IEKU::OID

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà OID** imposta o recupera una stringa che contiene un valore stringa OID EKU come definito in Wincrypt.h.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EKU.OID As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che contiene il valore stringa OID EKU come definito in Wincrypt.h.

## <a name="remarks"></a>Commenti

Questa proprietà non usa [**l'oggetto OID**](oid.md) introdotto in CAPICOM 2.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
