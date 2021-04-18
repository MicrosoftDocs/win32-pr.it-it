---
description: 'Altre informazioni su: metodo Update. SaveAndGotoBookmark'
title: Update. SaveAndGotoBookmark, metodo
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
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307791"
---
# <a name="updatesaveandgotobookmark-method"></a>Update. SaveAndGotoBookmark, metodo

Aggiornare TableID e posizionare TableID sul record che è stato modificato. Questa operazione può essere utile quando si inserisce un record perché per impostazione predefinita il TableID rimane nella posizione precedente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Salva è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record. Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Update](./update-class.md)

[Aggiornare i membri](./update-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
