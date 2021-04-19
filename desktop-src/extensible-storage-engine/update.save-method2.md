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
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389030"
---
# <a name="updatesave-method"></a><span data-ttu-id="8e2c6-103">Metodo Update. Save</span><span class="sxs-lookup"><span data-stu-id="8e2c6-103">Update.Save method</span></span>

<span data-ttu-id="8e2c6-104">Aggiornare il TableID.</span><span class="sxs-lookup"><span data-stu-id="8e2c6-104">Update the tableid.</span></span>

<span data-ttu-id="8e2c6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e2c6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e2c6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e2c6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2c6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2c6-107">Syntax</span></span>

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

## <a name="remarks"></a><span data-ttu-id="8e2c6-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8e2c6-108">Remarks</span></span>

<span data-ttu-id="8e2c6-109">Salva è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8e2c6-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="8e2c6-110">L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="8e2c6-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="8e2c6-111">Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8e2c6-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="8e2c6-112">Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="8e2c6-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e2c6-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e2c6-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e2c6-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8e2c6-114">Reference</span></span>

[<span data-ttu-id="8e2c6-115">Classe Update</span><span class="sxs-lookup"><span data-stu-id="8e2c6-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="8e2c6-116">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="8e2c6-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="8e2c6-117">Salva overload</span><span class="sxs-lookup"><span data-stu-id="8e2c6-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="8e2c6-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8e2c6-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
