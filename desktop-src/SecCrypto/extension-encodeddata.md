---
description: Recupera i dati codificati per l'estensione.
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: Proprietà Extension. EncodedData
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
ms.openlocfilehash: 2153c97d523693a0a1ea13f92135a17591ce68d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326527"
---
# <a name="extensionencodeddata-property"></a>Proprietà Extension. EncodedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **EncodedData** recupera i dati codificati per l'estensione.

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
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
