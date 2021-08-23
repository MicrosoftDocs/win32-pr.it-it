---
description: Recupera un valore booleano che indica se il bit keyCertSign è impostato.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Proprietà KeyUsage.IsKeyCertSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61c5ca1e9ae36159293e1e9afe1f79b5ff30cbd659b01a400797ae35aac8873c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515881"
---
# <a name="keyusageiskeycertsignenabled-property"></a>Proprietà KeyUsage.IsKeyCertSignEnabled

\[La **proprietà IsKeyCertSignEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà IsKeyCertSignEnabled** recupera un valore booleano che indica se il bit keyCertSign è impostato.

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** il bit keyCertSign è impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
