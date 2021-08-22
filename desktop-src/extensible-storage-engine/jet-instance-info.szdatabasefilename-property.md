---
description: 'Altre informazioni su: JET_INSTANCE_INFO.szDatabaseFileName'
title: JET_INSTANCE_INFO.szDatabaseFileName
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bcf0360ea2c901c1fc68c97c8b29f222c1df2e9a65dacf87297e3b560ece0d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119272431"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a>JET_INSTANCE_INFO.szDatabaseFileName

Ottiene una raccolta di stringhe, ognuna delle quali contiene il nome file di un database collegato all'istanza del database. La matrice contiene elementi cDatabases.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\>  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INSTANCE_INFO classe](./jet-instance-info-class.md)

[JET_INSTANCE_INFO membri](./jet-instance-info-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
