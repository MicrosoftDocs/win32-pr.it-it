---
description: Imposta o recupera l'intervallo di tempo prima che un URL venga determinato come irraggiungibile.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Proprietà CertificateStatus. UrlRetrievalTimeout
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
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324137"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>Proprietà CertificateStatus. UrlRetrievalTimeout

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **UrlRetrievalTimeout** imposta o recupera l'intervallo di tempo prima che un URL venga determinato come irraggiungibile.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Valore proprietà

Il numero di secondi prima che un URL venga determinato come irraggiungibile.

## <a name="remarks"></a>Commenti

Se questa proprietà non è impostata, il timeout predefinito è 15 secondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
