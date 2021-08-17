---
description: Recupera una stringa contenente il nome dell'autorità emittente del certificato.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Proprietà Certificate.IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f4404a105748a79ef942f37c088a5436fc3eeea0784bb6ff814dd0782262dcf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771581"
---
# <a name="certificateissuername-property"></a>Proprietà Certificate.IssuerName

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà IssuerName** recupera una stringa contenente il nome dell'autorità emittente del certificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente il nome dell'autorità emittente del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
