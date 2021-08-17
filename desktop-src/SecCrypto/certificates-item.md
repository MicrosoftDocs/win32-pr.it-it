---
description: Recupera un oggetto Certificate che rappresenta il certificato indicizzato della raccolta. Si tratta della proprietà predefinita.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificates.Item - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927f52570b515c6699458cfb802b5c315201d401e9bcf5e0be76ab41863bd47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770540"
---
# <a name="certificatesitem-property"></a>Certificates.Item - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Item** recupera un oggetto [**Certificate**](certificate.md) che rappresenta il certificato indicizzato della raccolta. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Certificate**](certificate.md) che rappresenta il certificato indicizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificati**](certificates.md)
</dt> </dl>

 

 
