---
description: Altre informazioni sul metodo Update.SaveAndGotoBookmark
title: Metodo Update.SaveAndGotoBookmark
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 566be9b1af403a794b6ac87259a0fd6b6c0fea46c0b45287c536f336ee734b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106955"
---
# <a name="updatesaveandgotobookmark-method"></a>Metodo Update.SaveAndGotoBookmark

Aggiornare il tableid e posizionare il tableid nel record modificato. Ciò può essere utile quando si inserisce un record perché per impostazione predefinita il tableid rimane nella posizione precedente.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>Osservazioni

Il salvataggio è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record. Infine, viene chiamato Update per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da Update o non durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Update](./update-class.md)

[Aggiornare i membri](./update-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
