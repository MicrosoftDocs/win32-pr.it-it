---
description: 'Altre informazioni su: Proprietà JET_INDEXLIST. columnidcKey'
title: Proprietà JET_INDEXLIST. columnidcKey
TOCTitle: 'columnidcKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidckey(v=EXCHG.10)
ms:contentKeyID: 55103598
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 884bfaaea30600919a905616cd0e808541f56ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319674"
---
# <a name="jet_indexlistcolumnidckey-property"></a>Proprietà JET_INDEXLIST. columnidcKey

Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di chiavi univoche nell'indice. Questo valore non è aggiornato e viene aggiornato solo da "API. JetComputeStats". La colonna è di tipo [Long](./jet-coltyp-enumeration.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property columnidcKey As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcKey
```

``` csharp
public JET_COLUMNID columnidcKey { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Membri JET_INDEXLIST](./jet-indexlist-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
