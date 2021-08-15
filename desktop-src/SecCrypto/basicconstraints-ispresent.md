---
description: Recupera un valore booleano che indica se l'estensione dei vincoli di base è presente. Si tratta della proprietà predefinita.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints.IsPresent - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 646d7988b24d9ad03e55bb7ee4401875c42f7b779a81e1b80a611aaae18a93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773023"
---
# <a name="basicconstraintsispresent-property"></a>BasicConstraints.IsPresent - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **proprietà IsPresent** recupera un valore booleano che indica se l'estensione dei vincoli di base è presente. Si tratta della proprietà predefinita.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, è presente l'estensione dei vincoli di base.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di base**](basicconstraints.md)
</dt> </dl>

 

 
