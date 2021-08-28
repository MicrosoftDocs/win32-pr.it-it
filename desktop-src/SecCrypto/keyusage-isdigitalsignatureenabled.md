---
description: Recupera un valore booleano che indica se il bit digitalSignature è impostato.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: KeyUsage.IsDigitalSignatureEnabled - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 963fc78243cf235fe0975fae203e17d1d4f6e71bb909259c7c83acc4fe9e5f07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080651"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a>KeyUsage.IsDigitalSignatureEnabled - proprietà

\[La **proprietà IsDigitalSignatureEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà IsDigitalSignatureEnabled** recupera un valore booleano che indica se il bit digitalSignature è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** viene impostato il bit digitalSignature.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
