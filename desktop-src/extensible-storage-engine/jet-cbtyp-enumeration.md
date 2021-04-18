---
description: 'Altre informazioni su: Enumerazione JET_cbtyp'
title: Enumerazione JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308516"
---
# <a name="jet_cbtyp-enumeration"></a>Enumerazione JET_cbtyp

Tipo di stato di avanzamento segnalato.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
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
<td>Null</td>
<td>Questo callback è riservato e sempre considerato non valido.</td>
</tr>
<tr class="even">
<td></td>
<td>Finalize</td>
<td>Una colonna finalizzabile è scesa a zero.</td>
</tr>
<tr class="odd">
<td></td>
<td>PrimaDiInserire</td>
<td>Questo callback si verificherà immediatamente prima dell'inserimento di un nuovo record in una tabella tramite una chiamata a JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>Questo callback si verificherà subito dopo l'inserimento di un nuovo record in una tabella tramite una chiamata a JetUpdate, ma prima della restituzione di JetUpdate.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Questo callback si verificherà immediatamente prima di un record esistente in una tabella modificata da una chiamata a JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Questo callback si verifica subito dopo la modifica di un record esistente in una tabella da una chiamata a JetUpdate, ma prima che JetUpdate restituisca.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Questo callback si verificherà immediatamente prima che un record esistente in una tabella venga eliminato da una chiamata a JetDelete.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Questo callback si verificherà subito dopo l'eliminazione di un record esistente in una tabella da una chiamata a JetDelete.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Questo callback si verifica quando il motore deve recuperare il valore predefinito definito dall'utente di una colonna dall'applicazione. Questo callback è essenzialmente un'implementazione limitata di JetRetrieveColumn valutata dall'applicazione. Per un valore predefinito definito dall'utente può essere restituito un massimo di un valore di colonna.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Questo callback si verifica quando la deframmentazione in linea di un database iniziata da JetDefragment è stata interrotta a causa del completamento del processo o del raggiungimento del limite di tempo.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>Questo callback si verifica quando l'applicazione deve eseguire la pulizia dell'handle di contesto per l'archiviazione locale associata a un cursore rilasciato dal motore di database. Per ulteriori informazioni, vedere JetSetLS. Il delegato per questo motivo di callback viene configurato per mezzo di JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>Questo callback si verificherà come il risultato della necessità che l'applicazione ripulisca l'handle di contesto per l'archiviazione locale associata a una tabella rilasciata dal motore di database. Per ulteriori informazioni, vedere JetSetLS. Il delegato per questo motivo di callback viene configurato per mezzo di JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
