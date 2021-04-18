---
description: 'Altre informazioni su: metodo API. JetOpenTempTable3'
title: Metodo Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318477"
---
# <a name="apijetopentemptable3-method"></a>Metodo Api.JetOpenTempTable3

Crea una tabella temporanea con un solo indice. Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale. Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - colonne  
    Tipo \[\]  
    
    Definizioni di colonna per le colonne create nella tabella temporanea.

<!-- end list -->

  - numColumns  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di definizioni di colonna.

<!-- end list -->

  - unicodeindex  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    ID delle impostazioni locali e flag di normalizzazione che verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. Quando non è presente, vengono usate le opzioni predefinite.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Opzioni per la creazione di tabelle.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Restituisce il TableID della tabella temporanea. La chiusura di questo TableID con [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera le risorse associate alla tabella temporanea.

<!-- end list -->

  - columnIDs  
    Tipo \[\]  
    
    Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea. Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
