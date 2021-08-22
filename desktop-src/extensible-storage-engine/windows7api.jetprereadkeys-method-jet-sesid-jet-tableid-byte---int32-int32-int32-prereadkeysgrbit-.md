---
description: 'Altre informazioni su: Metodo Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, Byte[][], Int32, Int32, Int32, PrereadKeysGrbit)'
title: Metodo Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, Byte[][], Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft.Isam.Esent.Interop.Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6880e7fa1520f55f4cf1dd8300c4f7b75002a84e164cd80e1be341a0548bd9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470891"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a>Metodo Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, PrereadKeysGrbit)

Se i record con le chiavi specificate non sono presenti nella cache del buffer, avviare le letture asincrone per portare i record nella cache del buffer del database.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
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

  - chiavi  
    digitare: \[\]  
    
    Chiavi da pre-leggere. Le chiavi devono essere ordinate.

<!-- end list -->

  - keyLengths  
    digitare: \[\]  
    
    Lunghezze delle chiavi da pre-leggere.

<!-- end list -->

  - keyCount  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero massimo di chiavi da pre-leggere.

<!-- end list -->

  - keysPreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di chiavi da pre-leggere effettivamente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Opzioni di prelettura. Consente di specificare la direzione della prelettura.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows7Api](./windows7api-class.md)

[Membri di Windows7Api](./windows7api-members.md)

[Overload di JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
