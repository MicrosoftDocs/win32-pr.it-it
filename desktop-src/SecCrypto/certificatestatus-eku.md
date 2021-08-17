---
description: Restituisce l'oggetto EKU utilizzato per compilare l'oggetto Chain.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Metodo CertificateStatus.EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 63ddc2cd793c786cff1f7c5bb983cdba525fb52f940723f826ab4b44b89bf1ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770292"
---
# <a name="certificatestatuseku-method"></a>Metodo CertificateStatus.EKU

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo EKU** restituisce l'oggetto [**EKU**](eku.md) usato per compilare [**l'oggetto Chain.**](chain.md)

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un [**oggetto EKU**](eku.md) che indica l'impostazione di utilizzo della chiave estesa del [*certificato*](../secgloss/c-gly.md). L'impostazione EKU stabilisce l'uso valido di un certificato. È possibile impostare un **solo oggetto EKU** per ogni certificato.

## <a name="remarks"></a>Commenti

Il [**metodo CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) fornisce la stessa funzionalità di questo metodo, ma consente di impostare molte impostazioni anziché una sola. Se la [**raccolta OID**](oids.md) restituita dal **metodo ApplicationPolicies** contiene uno o più [**oggetti OID,**](oid.md) l'oggetto [**EKU**](eku.md) restituito da questo metodo viene ignorato. Usare il **metodo ApplicationPolicies** anziché questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
