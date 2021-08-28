---
description: Restituisce una raccolta OID che rappresenta i criteri certificato utilizzati per creare l'oggetto Chain.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Metodo CertificateStatus.CertificatePolicies
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
ms.openlocfilehash: e4d6507446bf15d00d8e388699ee0c0892c8755b94913d18657634311db57ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126711"
---
# <a name="certificatestatuscertificatepolicies-method"></a>Metodo CertificateStatus.CertificatePolicies

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo CertificatePolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri certificato usati per creare [**l'oggetto Chain.**](chain.md)

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Raccolta [**di OID.**](oids.md) Ogni [**oggetto OID**](oid.md) nella raccolta rappresenta un OID dei criteri del certificato.

## <a name="remarks"></a>Commenti

Aggiungere gli OID dei criteri di certificato alla raccolta per specificare i criteri del certificato che devono essere usati per creare la catena di certificati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
