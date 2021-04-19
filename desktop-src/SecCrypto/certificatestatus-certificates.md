---
description: Imposta o recupera la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Proprietà CertificateStatus. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326043"
---
# <a name="certificatestatuscertificates-property"></a>Proprietà CertificateStatus. Certificates

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **Certificates** imposta o recupera la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Certificates**](certificates.md) che rappresenta la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
