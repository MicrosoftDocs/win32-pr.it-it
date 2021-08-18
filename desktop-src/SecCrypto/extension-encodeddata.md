---
description: Recupera i dati codificati per l'estensione.
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: Extension.EncodedData - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4783a6f598bf094ca2bca10b2abcb7e222e34ffc5956b2dc6f0977416e9e99a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006949"
---
# <a name="extensionencodeddata-property"></a>Extension.EncodedData - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà EncodedData** recupera i dati codificati per l'estensione.

## <a name="syntax"></a>Sintassi


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**EncodedData**](encodeddata.md) che rappresenta i dati dell'estensione del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
