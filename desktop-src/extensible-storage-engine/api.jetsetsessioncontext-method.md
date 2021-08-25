---
description: Altre informazioni sul metodo Api.JetSetSessionContext
title: Metodo Api.JetSetSessionContext
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5530988aff70589493645afb2bf0b78da63470a1f48d1619913fbfdf8d8c8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977601"
---
# <a name="apijetsetsessioncontext-method"></a>Metodo Api.JetSetSessionContext

Associa una sessione al thread corrente usando l'handle di contesto specificato. Questa associazione sostituisce il requisito predefinito del motore che una transazione per una determinata sessione deve essere eseguita interamente nello stesso thread. Usare [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) per rimuovere l'associazione.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione su cui impostare il contesto.

<!-- end list -->

  - contesto  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contesto da impostare.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
