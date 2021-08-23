---
description: 'Altre informazioni su: Metodo Api.JetIdle'
title: Metodo Api.JetIdle
TOCTitle: 'JetIdle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIdle(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.IdleGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetidle(v=EXCHG.10)
ms:contentKeyID: 55100757
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98ae40ecc25fabb4fa6054417f30e6e358fc962bb05b192e03d1ea416d255211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117571"
---
# <a name="apijetidle-method"></a>Metodo Api.JetIdle

Esegue attività di pulizia inattive o controlla lo stato dell'archivio versioni in ESE.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetIdle ( _
    sesid As JET_SESID, _
    grbit As IdleGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim grbit As IdleGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetIdle(sesid, _
    grbit)
```

``` csharp
public static JET_wrn JetIdle(
    JET_SESID sesid,
    IdleGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.IdleGrbit](./idlegrbit-enumeration.md)  
    
    Combinazione di flag JetIdleGrbit.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di errore se l'operazione non riesce.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
