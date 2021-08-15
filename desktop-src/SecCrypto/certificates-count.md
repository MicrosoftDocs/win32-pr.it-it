---
description: Recupera il numero di oggetti Certificate nella raccolta.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Certificates.Count - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770550"
---
# <a name="certificatescount-property"></a>Certificates.Count - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Count** recupera il numero di oggetti [**Certificate**](certificate.md) nella raccolta.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di [**oggetti Certificate**](certificate.md) nella raccolta. Ogni **oggetto Certificate** rappresenta un singolo certificato nella raccolta.

## <a name="remarks"></a>Commenti

CAPICOM supporta solo un singolo certificato per [*l'smart card*](../secgloss/s-gly.md) archiviazione. Anche se l smart card store contiene più di un certificato, questa proprietà conterrà 1. Per altre informazioni sull'archivio smart card, vedere il membro **\_ CAPICOM SMART \_ CARD USER \_ \_ STORE** dell'enumerazione [**CAPICOM STORE \_ \_ LOCATION.**](capicom-store-location.md)

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

 

 
