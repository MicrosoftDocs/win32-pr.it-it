---
description: 'Altre informazioni su: metodo Update. Save'
title: Metodo Update. Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57693d3952f011127e60fdfb70dd2352c2f15207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526796"
---
# <a name="updatesave-method"></a><span data-ttu-id="b76d0-103">Metodo Update. Save</span><span class="sxs-lookup"><span data-stu-id="b76d0-103">Update.Save method</span></span>

<span data-ttu-id="b76d0-104">Aggiornare il TableID.</span><span class="sxs-lookup"><span data-stu-id="b76d0-104">Update the tableid.</span></span>

<span data-ttu-id="b76d0-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b76d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b76d0-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b76d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b76d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b76d0-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="b76d0-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b76d0-108">Remarks</span></span>

<span data-ttu-id="b76d0-109">Salva è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b76d0-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="b76d0-110">L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="b76d0-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="b76d0-111">Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b76d0-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="b76d0-112">Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="b76d0-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="b76d0-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b76d0-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b76d0-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b76d0-114">Reference</span></span>

[<span data-ttu-id="b76d0-115">Classe Update</span><span class="sxs-lookup"><span data-stu-id="b76d0-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="b76d0-116">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="b76d0-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="b76d0-117">Salva overload</span><span class="sxs-lookup"><span data-stu-id="b76d0-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="b76d0-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b76d0-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
