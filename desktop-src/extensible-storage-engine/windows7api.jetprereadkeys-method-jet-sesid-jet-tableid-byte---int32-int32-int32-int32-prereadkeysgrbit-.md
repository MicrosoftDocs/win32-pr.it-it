---
description: 'Altre informazioni su: Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit)'
title: Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. esent. Interop. Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
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
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226385"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a>Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte \[ \] \[ \] , Int32, Int32, Int32, Int32, PrereadKeysGrbit)

Se i record con le chiavi specificate non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
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

  - chiavi  
    Tipo \[\]  
    
    Chiavi da preleggere. Le chiavi devono essere ordinate.

<!-- end list -->

  - Lunghezze di pagina  
    Tipo \[\]  
    
    Lunghezza delle chiavi da preleggere.

<!-- end list -->

  - keyIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Indice della prima chiave nella matrice di chiavi da leggere.

<!-- end list -->

  - Numero di conteggio  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero massimo di chiavi da preleggere.

<!-- end list -->

  - keysPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di chiavi da preleggere effettivamente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Windows7. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Opzioni di prelettura. Utilizzato per specificare la direzione della prelettura.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows7Api](./windows7api-class.md)

[Membri di Windows7Api](./windows7api-members.md)

[Overload JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
