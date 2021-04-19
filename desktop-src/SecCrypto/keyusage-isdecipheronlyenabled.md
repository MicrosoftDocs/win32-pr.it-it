---
description: Recupera un valore booleano che indica se il bit decipherOnly è impostato.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: Proprietà DataUsage. IsDecipherOnlyEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5ca72348220d6943ad367e88f404e0f3163f4c42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323962"
---
# <a name="keyusageisdecipheronlyenabled-property"></a>Proprietà DataUsage. IsDecipherOnlyEnabled

\[La proprietà **IsDecipherOnlyEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **IsDecipherOnlyEnabled** recupera un valore booleano che indica se il bit decipherOnly è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, viene impostato il bit decipherOnly.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
