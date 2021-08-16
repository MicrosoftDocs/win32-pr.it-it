---
description: Recupera un valore booleano che indica se l'estensione del vincolo di base è contrassegnata come critica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: BasicConstraints.IsCritical - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3918a89719195e6c8672a0dab13c62af3e866f8fd5695df20f0126f7831f369c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773033"
---
# <a name="basicconstraintsiscritical-property"></a>BasicConstraints.IsCritical - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **proprietà IsCritical** recupera un valore booleano che indica se l'estensione del vincolo di base è contrassegnata come critica.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true,** l'estensione del vincolo di base è contrassegnata come critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
