---
description: Restituisce una raccolta di OID che rappresenta i criteri dell'applicazione usati per creare l'oggetto Chain.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Metodo CertificateStatus.ApplicationPolicies
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
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770441"
---
# <a name="certificatestatusapplicationpolicies-method"></a>Metodo CertificateStatus.ApplicationPolicies

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo ApplicationPolicies** restituisce una [**raccolta OID**](oids.md) che rappresenta i criteri dell'applicazione usati per creare [**l'oggetto Chain.**](chain.md)

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Raccolta [**di OID.**](oids.md) Ogni [**oggetto OID**](oid.md) nella raccolta rappresenta un OID dei criteri dell'applicazione.

## <a name="remarks"></a>Commenti

Aggiungere gli OID dei criteri dell'applicazione alla raccolta per specificare i criteri dell'applicazione da usare per compilare la catena di certificati attendibili. Se la raccolta contiene almeno un [**oggetto OID,**](oid.md) l'oggetto [**EKU**](eku.md) restituito dal [**metodo CertificateStatus.EKU**](certificatestatus-eku.md) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
