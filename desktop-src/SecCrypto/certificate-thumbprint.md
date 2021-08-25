---
description: Recupera una stringa esadecimale che contiene l'hash SHA-1 del certificato.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Proprietà Certificate.Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 64748f3eb8b9623ea7c07a7428f29b30276c34ab38631fdbf210b25b5be92a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878161"
---
# <a name="certificatethumbprint-property"></a>Proprietà Certificate.Thumbprint

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Identificazione** personale recupera una stringa esadecimale che contiene l'hash [*SHA-1*](../secgloss/s-gly.md) del certificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Valore proprietà

Stringa esadecimale che contiene l'hash SHA-1 del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
