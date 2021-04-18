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
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="d7006-103">Update. SaveAndGotoBookmark, metodo</span><span class="sxs-lookup"><span data-stu-id="d7006-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="d7006-104">Aggiornare TableID e posizionare TableID sul record che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="d7006-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="d7006-105">Questa operazione può essere utile quando si inserisce un record perché per impostazione predefinita il TableID rimane nella posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="d7006-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="d7006-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d7006-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d7006-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d7006-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d7006-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7006-108">Syntax</span></span>

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

## <a name="remarks"></a><span data-ttu-id="d7006-109">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d7006-109">Remarks</span></span>

<span data-ttu-id="d7006-110">Salva è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d7006-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d7006-111">L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="d7006-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="d7006-112">Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d7006-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="d7006-113">Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="d7006-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7006-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7006-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d7006-115">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d7006-115">Reference</span></span>

[<span data-ttu-id="d7006-116">Classe Update</span><span class="sxs-lookup"><span data-stu-id="d7006-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="d7006-117">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="d7006-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="d7006-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d7006-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
