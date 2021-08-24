---
description: Altre informazioni sul metodo Windows8Api.PrereadKeyRanges
title: Metodo Windows8Api.PrereadKeyRanges (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02328ddc47daec4fbd98f88222dd7519053ed92aa64d2a0048782340d626b03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452691"
---
# <a name="windows8apiprereadkeyranges-method"></a>Metodo Windows8Api.PrereadKeyRanges

Se i record con gli intervalli di chiavi specificati non sono presenti nella cache del buffer, avviare le letture asincrone per portare i record nella cache del buffer del database.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da usare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabella su cui eseguire le prelettura.

<!-- end list -->

  - keysStart  
    digitare: \[\]  
    
    Inizio degli intervalli di chiavi da pre-leggere.

<!-- end list -->

  - keyStartLengths  
    digitare: \[\]  
    
    Lunghezze delle chiavi di inizio da pre-leggere.

<!-- end list -->

  - keysEnd  
    digitare: \[\]  
    
    Fine degli intervalli di chiavi da pre-leggere.

<!-- end list -->

  - keyEndLengths  
    digitare: \[\]  
    
    Lunghezze delle chiavi finali da pre-leggere.

<!-- end list -->

  - rangeIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Indice del primo intervallo di chiavi nella matrice da leggere.

<!-- end list -->

  - rangeCount  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero massimo di intervalli di chiavi da pre-leggere.

<!-- end list -->

  - rangesPreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di chiavi effettivamente prelette.

<!-- end list -->

  - columnsPreread  
    digitare: \[\]  
    
    Elenco di ID di colonna per le colonne con valori lunghi da pre-leggere.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Opzioni di prelettura. Consente di specificare la direzione della prelettura.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows8Api](./windows8api-class.md)

[Membri di Windows8Api](./windows8api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
