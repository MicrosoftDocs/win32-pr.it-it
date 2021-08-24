---
description: Altre informazioni sul metodo DurableCommitCallback.ReleaseResource
title: Metodo DurableCommitCallback.ReleaseResource (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 758c27b1b3a67b91b7921276ec26e9c9776b65255c4cfa88d32b839f9950c2af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725271"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>Metodo DurableCommitCallback.ReleaseResource

Libera la sessione di commit durevole.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a>Osservazioni

Non provare a impostare il parametro di istanza su Null, perché il callback viene eliminato dopo JetTerm e il callback non può essere impostato dopo JetTerm.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe DurableCommitCallback](./durablecommitcallback-class.md)

[Membri durableCommitCallback](./durablecommitcallback-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
