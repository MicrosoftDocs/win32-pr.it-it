---
description: Restituisce un valore booleano che indica se l'estensione EKU è presente. Si tratta della proprietà predefinita.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage.IsPresent - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c561e6c848380326151af12aebf584fb53eb7332c8e6c0d61074da03f7d3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007339"
---
# <a name="extendedkeyusageispresent-property"></a>ExtendedKeyUsage.IsPresent - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà IsPresent** restituisce un valore booleano che indica se l'estensione EKU è presente. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** l'estensione EKU è presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
