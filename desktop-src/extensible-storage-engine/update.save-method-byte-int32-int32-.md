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
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="d09b6-103">Metodo Update. Save (byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="d09b6-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="d09b6-104">Aggiornare il TableID.</span><span class="sxs-lookup"><span data-stu-id="d09b6-104">Update the tableid.</span></span>

<span data-ttu-id="d09b6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d09b6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d09b6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d09b6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d09b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d09b6-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="d09b6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d09b6-108">Parameters</span></span>

  - <span data-ttu-id="d09b6-109">segnalibro</span><span class="sxs-lookup"><span data-stu-id="d09b6-109">bookmark</span></span>  
    <span data-ttu-id="d09b6-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="d09b6-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="d09b6-111">Restituisce il segnalibro del record aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d09b6-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="d09b6-112">Può essere Null.</span><span class="sxs-lookup"><span data-stu-id="d09b6-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="d09b6-113">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="d09b6-113">bookmarkSize</span></span>  
    <span data-ttu-id="d09b6-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d09b6-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d09b6-115">Dimensioni del buffer dei segnalibri.</span><span class="sxs-lookup"><span data-stu-id="d09b6-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="d09b6-116">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="d09b6-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="d09b6-117">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d09b6-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d09b6-118">Restituisce le dimensioni effettive del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="d09b6-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09b6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d09b6-119">Remarks</span></span>

<span data-ttu-id="d09b6-120">Salva è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d09b6-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d09b6-121">L'aggiornamento viene avviato chiamando la creazione di un oggetto Update e quindi chiamando JetSetColumn o JetSetColumns una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="d09b6-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="d09b6-122">Infine, viene chiamato l'aggiornamento per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d09b6-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="d09b6-123">Gli indici vengono aggiornati solo tramite l'aggiornamento o e non durante JetSetColumn o JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="d09b6-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="d09b6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d09b6-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d09b6-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d09b6-125">Reference</span></span>

[<span data-ttu-id="d09b6-126">Classe Update</span><span class="sxs-lookup"><span data-stu-id="d09b6-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="d09b6-127">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="d09b6-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="d09b6-128">Salva overload</span><span class="sxs-lookup"><span data-stu-id="d09b6-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="d09b6-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d09b6-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
