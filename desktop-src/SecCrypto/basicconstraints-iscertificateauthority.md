---
description: Recupera un valore booleano che indica se il certificato è per un'autorità di certificazione (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints.IsCertificateAuthority - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879761"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>BasicConstraints.IsCertificateAuthority - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **proprietà IsCertificateAuthority** recupera un valore booleano che indica se il certificato è per un'autorità [*di certificazione*](../secgloss/c-gly.md) (CA).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **True,** il certificato deve essere usato solo da una CA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
