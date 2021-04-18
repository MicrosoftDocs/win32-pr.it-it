---
description: Recupera l'OID del criterio. Si tratta della proprietà predefinita.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Proprietà PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324842"
---
# <a name="policyinformationoid-property"></a>Proprietà PolicyInformation. OID

\[La proprietà **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]

La proprietà **OID** recupera l'OID del criterio. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Valore proprietà

Identificatore di oggetto del criterio come oggetto [**OID**](oid.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
