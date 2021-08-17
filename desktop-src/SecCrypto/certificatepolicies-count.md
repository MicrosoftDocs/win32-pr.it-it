---
description: Recupera il numero di oggetti PolicyInformation nella raccolta.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies.Count - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 405fbc928f6ff553abe3cd55d3f6e08a1aed13ef46093f912b6b08af45ec2c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771049"
---
# <a name="certificatepoliciescount-property"></a>CertificatePolicies.Count - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri certificato per recuperare i criteri del certificato.\]

La **proprietà Count** recupera il numero di oggetti [**PolicyInformation**](policyinformation.md) nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di [**oggetti PolicyInformation**](policyinformation.md) nella raccolta. Ogni **oggetto PolicyInformation** rappresenta un singolo criterio certificato nella raccolta.

## <a name="remarks"></a>Commenti

La **proprietà Count** può essere usata per specificare l'ultimo oggetto [**PolicyInformation**](policyinformation.md) nella raccolta quando si recupera un oggetto **PolicyInformation** specifico usando la proprietà [**CertificatePolicies.Item.**](certificatepolicies-item.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
