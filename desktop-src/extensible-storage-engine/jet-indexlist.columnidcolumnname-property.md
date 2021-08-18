---
description: 'Altre informazioni su: JET_INDEXLIST.columnidcolumnname'
title: JET_INDEXLIST.columnidcolumnname
TOCTitle: 'columnidcolumnname property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcolumnname(v=EXCHG.10)
ms:contentKeyID: 55103662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af517a86946c6115728f5c53608e8925afd049228c6edfb5f47fb2384a2b99f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116041"
---
# <a name="jet_indexlistcolumnidcolumnname-property"></a>JET_INDEXLIST.columnidcolumnname

Ottiene il columnid della colonna nella tabella temporanea in cui è archiviato il grbit applicato alla colonna indicizzata. Vedere [IndexKeyGrbit](./indexkeygrbit-enumeration.md). La colonna è di tipo [Text](./jet-coltyp-enumeration.md).

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property columnidcolumnname As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcolumnname
```

``` csharp
public JET_COLUMNID columnidcolumnname { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INDEXLIST classe](./jet-indexlist-class.md)

[JET_INDEXLIST membri](./jet-indexlist-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
