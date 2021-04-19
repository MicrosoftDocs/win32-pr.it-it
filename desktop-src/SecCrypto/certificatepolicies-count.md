---
description: Recupera il numero di oggetti PolicyInformation nell'insieme.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Proprietà CertificatePolicies. Count
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
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333020"
---
# <a name="certificatepoliciescount-property"></a>Proprietà CertificatePolicies. Count

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]

La proprietà **count** Recupera il numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme. Ogni oggetto **PolicyInformation** rappresenta un singolo criterio del certificato nella raccolta.

## <a name="remarks"></a>Commenti

La proprietà **count** può essere usata per specificare l'ultimo oggetto [**PolicyInformation**](policyinformation.md) nella raccolta durante il recupero di un oggetto **PolicyInformation** specifico usando la proprietà [**CertificatePolicies. Item**](certificatepolicies-item.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
