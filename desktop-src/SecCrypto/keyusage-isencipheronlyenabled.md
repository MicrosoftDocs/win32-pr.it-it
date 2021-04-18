---
description: Recupera un valore booleano che indica se il bit encipherOnly è impostato.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: Proprietà DataUsage. IsEncipherOnlyEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323960"
---
# <a name="keyusageisencipheronlyenabled-property"></a>Proprietà DataUsage. IsEncipherOnlyEnabled

\[La proprietà **IsEncipherOnlyEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **IsEncipherOnlyEnabled** recupera un valore booleano che indica se il bit encipherOnly è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, viene impostato il bit encipherOnly.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
