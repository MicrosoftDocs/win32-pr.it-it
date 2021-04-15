---
description: 'Altre informazioni su: metodo Update. Save (byte, Int32, Int32)'
title: Metodo Update. Save (byte, Int32, Int32)
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
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485156"
---
# <a name="updatesave-method-byte--int32-int32"></a>Metodo Update. Save (byte, Int32, Int32)

Aggiornare il TableID.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo \[\]  
    
    Restituisce il segnalibro del record aggiornato. Può essere Null.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer dei segnalibri.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni effettive del segnalibro.

## <a name="remarks"></a>Commenti

Salva è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record. Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Update](./update-class.md)

[Aggiornare i membri](./update-members.md)

[Salva overload](./update.save-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
