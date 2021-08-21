---
description: 'Altre informazioni su: Metodo Api.JetEnumerateColumns'
title: Metodo Api.JetEnumerateColumns
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 713b02835aa063e888a2385df9bd8abdff9af1300a2e9885c06e995f2b814bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042709"
---
# <a name="apijetenumeratecolumns-method"></a>Metodo Api.JetEnumerateColumns

Recupera in modo efficiente un set di colonne e i relativi valori dal record corrente di un cursore o dal buffer di copia del cursore. Le colonne e i valori recuperati possono essere limitati da un elenco di ID di colonna, numeri itagSequence e altre caratteristiche. Questa API di recupero colonna è univoca perché restituisce informazioni nella memoria allocata dinamicamente ottenuta usando un callback compatibile con la rialloca fornito dall'utente. Questa nuova flessibilità consente il recupero efficiente dei dati della colonna con caratteristiche specifiche, ad esempio dimensioni e molteplicità, sconosciute al chiamante. In questo modo si elimina la necessità di usare le modalità di individuazione di JetRetrieveColumn per determinare tali caratteristiche per configurare una chiamata finale a JetRetrieveColumn che recupererà correttamente i dati desiderati.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da cui recuperare i dati.

<!-- end list -->

  - numColumnids  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numeri di JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    digitare: \[\]  
    
    Matrice facoltativa di ID di colonna, ognuno con una matrice facoltativa di numeri itagSequence da enumerare.

<!-- end list -->

  - numColumnValues  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di valori di colonna recuperati.

<!-- end list -->

  - columnValues  
    digitare: \[\]  
    
    Restituisce i valori di colonna enumerati.

<!-- end list -->

  - allocator  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Callback utilizzato per allocare memoria.

<!-- end list -->

  - allocatorContext  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contesto per il callback di allocazione.

<!-- end list -->

  - maxDataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Imposta un limite sulla quantità di dati da restituire da una colonna long text o long binary. Questo parametro può essere utilizzato per impedire l'enumerazione di un valore di colonna estremamente grande.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Recuperare le opzioni.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Avviso o esito positivo.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
