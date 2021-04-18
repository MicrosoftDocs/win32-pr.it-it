---
description: 'Altre informazioni su: VistaApi. JetOpenTemporaryTable, metodo'
title: Metodo VistaApi. JetOpenTemporaryTable (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309651"
---
# <a name="vistaapijetopentemporarytable-method"></a>VistaApi. JetOpenTemporaryTable, metodo

Crea una tabella temporanea con un solo indice. Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale. Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - temporarytable  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)  
    
    Descrizione della tabella temporanea da creare in input. Dopo una chiamata con esito positivo, la struttura contiene l'handle per gli identificatori di tabella e colonna temporanei. Al termine [, usare JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) per liberare la tabella temporanea.

## <a name="remarks"></a>Commenti

Introdotta in Windows Vista. Usare [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) per le versioni precedenti di esent.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaApi](./vistaapi-class.md)

[Membri di VistaApi](./vistaapi-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
