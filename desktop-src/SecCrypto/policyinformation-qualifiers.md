---
description: Recupera una raccolta dei qualificatori del criterio.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Proprietà PolicyInformation. Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324841"
---
# <a name="policyinformationqualifiers-property"></a>PolicyInformation. Qualifiers (proprietà)

\[La proprietà **qualificatori** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]

La proprietà **Qualifiers** recupera una raccolta dei qualificatori del criterio.

## <a name="syntax"></a>Sintassi


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Valore proprietà

Il puntatore CPS (Certification Practice Statement) del criterio o i qualificatori delle notifiche utente come oggetto [**qualificatori**](qualifiers.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
