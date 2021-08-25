---
description: Recupera un valore booleano che indica se è presente l'estensione KeyUsage.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Proprietà KeyUsage.IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2eb962445717743512de396065304f70c31f02cfa4f3448a08a2731ed1fd377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992861"
---
# <a name="keyusageispresent-property"></a>Proprietà KeyUsage.IsPresent

\[La **proprietà IsPresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà IsPresent** recupera un valore booleano che indica se è presente [**l'estensione KeyUsage.**](keyusage.md)

Questa proprietà è la proprietà predefinita [**dell'oggetto KeyUsage.**](keyusage.md)

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** l'estensione KeyUsage è presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
