---
description: Restituisce una raccolta OID che rappresenta i criteri del certificato utilizzati per creare l'oggetto catena.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327637"
---
# <a name="certificatestatuscertificatepolicies-method"></a>CertificateStatus. CertificatePolicies, metodo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **CertificatePolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri del certificato utilizzati per creare l'oggetto [**Chain**](chain.md) .

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Raccolta [**OID**](oids.md) . Ogni oggetto [**OID**](oid.md) della raccolta rappresenta un OID del criterio del certificato.

## <a name="remarks"></a>Commenti

Aggiungere i criteri di certificato OID alla raccolta per specificare i criteri dei certificati che devono essere usati per compilare la catena di certificati attendibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
