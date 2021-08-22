---
description: Altre informazioni sul metodo Update.Save (Byte, Int32, Int32)
title: Metodo Update.Save (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e586177075a34f3832486a9ace4a919abaad65dad21c0e54eba47b79f207be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603541"
---
# <a name="updatesave-method-byte--int32-int32"></a>Metodo Update.Save (Byte, Int32, Int32)

Aggiornare il tableid.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parametri

  - segnalibro  
    digitare: \[\]  
    
    Restituisce il segnalibro del record aggiornato. Può essere Null.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Dimensione del buffer del segnalibro.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni effettive del segnalibro.

## <a name="remarks"></a>Commenti

Il salvataggio è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record. Infine, viene chiamato Update per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da Update o non durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Update](./update-class.md)

[Aggiornare i membri](./update-members.md)

[Salvare l'overload](./update.save-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
