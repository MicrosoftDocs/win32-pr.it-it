---
description: Recupera un valore booleano che indica se il vincolo di lunghezza del percorso è presente.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: Proprietà BasicConstraints.IsPathLenConstraintPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c6faf267508476f423efaff6b012a25114eca25e7bc21c51c51b9a3e66dde802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879731"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>Proprietà BasicConstraints.IsPathLenConstraintPresent

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **proprietà IsPathLenConstraintPresent** recupera un valore booleano che indica se il vincolo di lunghezza del percorso è presente.

## <a name="syntax"></a>Sintassi


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **True,** il vincolo di lunghezza del percorso è presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
