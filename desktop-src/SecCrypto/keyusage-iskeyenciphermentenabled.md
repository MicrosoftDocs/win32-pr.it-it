---
description: Recupera un valore booleano che indica se il bit keyEncipherment è impostato.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Proprietà DataUsage. IsKeyEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323948"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a>Proprietà DataUsage. IsKeyEnciphermentEnabled

\[La proprietà **IsKeyEnciphermentEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **IsKeyEnciphermentEnabled** recupera un valore booleano che indica se il bit keyEncipherment è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, viene impostato il bit keyEncipherment.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
