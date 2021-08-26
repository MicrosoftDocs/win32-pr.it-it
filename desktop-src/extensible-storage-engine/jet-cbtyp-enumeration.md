---
description: 'Altre informazioni su: enumerazione JET_cbtyp dati'
title: JET_cbtyp enumerazione
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
ms.openlocfilehash: 209d3ffe9721f51b8c2d510eecb5408ac66cdbeb58309d1f033e2d23730328ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116231"
---
# <a name="jet_cbtyp-enumeration"></a>JET_cbtyp enumerazione

Tipo di stato segnalato.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Questo callback è riservato e considerato sempre non valido.</td>
</tr>
<tr class="even">
<td></td>
<td>Finalize</td>
<td>Una colonna finalizzabile è passata a zero.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeInsert</td>
<td>Questo callback si verificherà subito prima dell'inserimento di un nuovo record in una tabella tramite una chiamata a JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>Afterinsert</td>
<td>Questo callback si verificherà subito dopo l'inserimento di un nuovo record in una tabella da una chiamata a JetUpdate ma prima che jetUpdate venga restituito.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Questo callback si verificherà subito prima che un record esistente in una tabella venga modificato da una chiamata a JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Questo callback si verificherà subito dopo che un record esistente in una tabella è stato modificato da una chiamata a JetUpdate ma prima della restituzione di JetUpdate.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Questo callback si verificherà subito prima che un record esistente in una tabella venga eliminato da una chiamata a JetDelete.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Questo callback si verificherà subito dopo l'eliminazione di un record esistente in una tabella tramite una chiamata a JetDelete.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Questo callback si verifica quando il motore deve recuperare il valore predefinito definito dall'utente di una colonna dall'applicazione. Questo callback è essenzialmente un'implementazione limitata di JetRetrieveColumn che viene valutata dall'applicazione. È possibile restituire un massimo di un valore di colonna per un valore predefinito definito dall'utente.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Questo callback si verifica quando la deframmentazione online di un database come avviato da JetDefragment è stata arrestata a causa del completamento del processo o del limite di tempo raggiunto.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>Questo callback si verifica quando l'applicazione deve pulire l'handle di contesto per l'Archiviazione locale associato a un cursore rilasciato dal motore di database. Per altre informazioni, vedere JetSetLS. Il delegato per questo motivo di callback viene configurato tramite JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>Questo callback si verificherà in seguito alla necessità dell'applicazione di pulire l'handle di contesto per il Archiviazione locale associato a una tabella rilasciata dal motore di database. Per altre informazioni, vedere JetSetLS. Il delegato per questo motivo di callback viene configurato tramite JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
