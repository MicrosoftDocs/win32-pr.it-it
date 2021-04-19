---
description: Recupera un valore booleano che indica se l'estensione per l'utilizzo di dati è presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Proprietà DataUsage. Presenter
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
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323945"
---
# <a name="keyusageispresent-property"></a>Proprietà DataUsage. Presenter

\[La proprietà **impresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **represent** recupera un valore booleano che indica se l'estensione per l' [**utilizzo di dati**](keyusage.md) è presente.

Questa proprietà è la proprietà predefinita dell'oggetto [**DataUsage**](keyusage.md) .

## <a name="syntax"></a>Sintassi


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, è presente l'estensione per l'utilizzo di dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
