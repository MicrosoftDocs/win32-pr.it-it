---
description: Restituisce una raccolta OID che rappresenta i criteri dell'applicazione utilizzati per creare l'oggetto catena.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. ApplicationPolicies, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326151"
---
# <a name="certificatestatusapplicationpolicies-method"></a>CertificateStatus. ApplicationPolicies, metodo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **ApplicationPolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri dell'applicazione utilizzati per creare l'oggetto [**catena**](chain.md) .

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Raccolta [**OID**](oids.md) . Ogni oggetto [**OID**](oid.md) della raccolta rappresenta un OID dei criteri dell'applicazione.

## <a name="remarks"></a>Commenti

Aggiungere i criteri dell'applicazione OID alla raccolta per specificare i criteri dell'applicazione da usare per compilare la catena di certificati attendibili. Se la raccolta contiene almeno un oggetto [**OID**](oid.md) , l'oggetto [**EKU**](eku.md) restituito dal metodo [**CertificateStatus. EKU**](certificatestatus-eku.md) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
