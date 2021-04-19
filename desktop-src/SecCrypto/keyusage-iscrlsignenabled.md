---
description: Recupera un valore booleano che indica se il bit bit crlsign è impostato.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: Proprietà DataUsage. IsCRLSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39bd8509ebc89719e5d06e5e60a300ec2cd9949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323964"
---
# <a name="keyusageiscrlsignenabled-property"></a>Proprietà DataUsage. IsCRLSignEnabled

\[La proprietà **IsCRLSignEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **IsCRLSignEnabled** recupera un valore booleano che indica se il bit bit crlsign è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, viene impostato il bit bit crlsign.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
