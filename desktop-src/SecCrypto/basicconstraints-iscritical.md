---
description: Recupera un valore booleano che indica se l'estensione di vincolo di base è contrassegnata come critica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Proprietà BasicConstraints. Critical
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
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331307"
---
# <a name="basicconstraintsiscritical-property"></a>Proprietà BasicConstraints. Critical

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La proprietà **ipocrita** recupera un valore booleano che indica se l'estensione di vincolo di base è contrassegnata come critica.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, l'estensione del vincolo di base è contrassegnata come critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
