---
description: Imposta o recupera l'intervallo di tempo prima che un URL venga determinato come non raggiungibile.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus.UrlRetrievalTimeout - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770091"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>CertificateStatus.UrlRetrievalTimeout - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà UrlRetrievalTimeout** imposta o recupera l'intervallo di tempo prima che un URL venga determinato come non raggiungibile.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di secondi prima che un URL venga determinato come non raggiungibile.

## <a name="remarks"></a>Commenti

Se questa proprietà non è impostata, il timeout predefinito è 15 secondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
