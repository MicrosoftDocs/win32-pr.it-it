---
description: Recupera il numero di oggetti EKU nell'insieme.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Proprietà EKU. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330911"
---
# <a name="ekuscount-property"></a>Proprietà EKU. Count

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **count** Recupera il numero di oggetti [**EKU**](eku.md) nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di oggetti [**EKU**](eku.md) nella raccolta. Ogni oggetto **EKU** rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.

## <a name="remarks"></a>Commenti

La proprietà **count** può essere usata per specificare l'ultimo oggetto [**EKU**](eku.md) in una raccolta durante il recupero di un oggetto **EKU** specifico usando la proprietà [**EKU. Item**](ekus-item.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
