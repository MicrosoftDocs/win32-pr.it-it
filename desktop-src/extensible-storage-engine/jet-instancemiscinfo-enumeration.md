---
description: 'Altre informazioni su: Enumerazione JET_InstanceMiscInfo dati'
title: JET_InstanceMiscInfo enumerazione (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_InstanceMiscInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_instancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 39516547
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f3e311eddaf2cf6bdb3a7e06ef2a3acd719696a47accd055725c44f9a2b25b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980001"
---
# <a name="jet_instancemiscinfo-enumeration"></a>JET_InstanceMiscInfo enumerazione

Livelli di informazioni [per JetGetInstanceMiscInfo(JET_INSTANCE, JET_SIGNATURE, JET_InstanceMiscInfo)](./vistaapi.jetgetinstancemiscinfo-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_InstanceMiscInfo
'Usage
Dim instance As JET_InstanceMiscInfo
```

``` csharp
[FlagsAttribute]
public enum JET_InstanceMiscInfo
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>LogSignature</td>
<td>Ottiene la firma del log delle transazioni associato a questa sequenza.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
