---
description: Altre informazioni sul metodo Api.JetOpenTempTable2
title: Metodo Api.JetOpenTempTable2
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9d2ec2f1bd4448003b2423f0a7ac17fbd0b091f2af32186455c545f2a890a4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117718662"
---
# <a name="apijetopentemptable2-method"></a>Metodo Api.JetOpenTempTable2

Crea una tabella temporanea con un singolo indice. Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle normali a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire rapidamente la rimozione dei duplicati sui set di record quando vi si accede in modo puramente sequenziale. Vedere anche [JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - colonne  
    digitare: \[\]  
    
    Definizioni di colonna per le colonne create nella tabella temporanea.

<!-- end list -->

  - Numcolumns  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di definizioni di colonna.

<!-- end list -->

  - lcid  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    ID delle impostazioni locali da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. È possibile usare qualsiasi impostazione locale purché nel computer language pack sia stata installata la versione appropriata.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Opzioni di creazione della tabella.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Restituisce l'ID di tabella della tabella temporanea. La chiusura di questo tableid [con JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera le risorse associate alla tabella temporanea.

<!-- end list -->

  - columnids  
    digitare: \[\]  
    
    Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea. Gli ID di colonna in questa matrice corrisponderanno esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni della matrice di input.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
