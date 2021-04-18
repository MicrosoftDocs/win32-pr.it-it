---
description: 'Altre informazioni su: Windows8Api. JetPrereadIndexRanges, metodo'
title: Metodo Windows8Api. JetPrereadIndexRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 986213a054dec54e92e4ecfe6fb0abd541b451ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308798"
---
# <a name="windows8apijetprereadindexranges-method"></a>Windows8Api. JetPrereadIndexRanges, metodo

Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.JetPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static void JetPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabella su cui eseguire le preletture.

<!-- end list -->

  - indexRanges  
    Tipo \[\]  
    
    Intervalli di chiavi da preleggere.

<!-- end list -->

  - rangeIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Indice del primo intervallo di chiavi nella matrice da leggere.

<!-- end list -->

  - rangeCount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero massimo di intervalli di chiavi da preleggere.

<!-- end list -->

  - rangesPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di chiavi effettivamente prelette.

<!-- end list -->

  - columnsPreread  
    Tipo \[\]  
    
    Elenco di ID di colonna per le colonne con valore esteso da preleggere.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Opzioni di prelettura. Utilizzato per specificare la direzione della prelettura.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows8Api](./windows8api-class.md)

[Membri di Windows8Api](./windows8api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
