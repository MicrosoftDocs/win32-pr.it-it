---
description: Restituisce la raccolta EKU per il certificato.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Proprietà ExtendedKeyUsage. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324239"
---
# <a name="extendedkeyusageekus-property"></a>Proprietà ExtendedKeyUsage. EKU

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **EKU** restituisce la raccolta [**EKU**](ekus.md) per il certificato.

## <a name="syntax"></a>Sintassi


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a>Valore proprietà

Raccolta [**EKU**](ekus.md) che contiene gli oggetti [**EKU**](eku.md) per il certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
