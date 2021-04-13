---
description: Contiene informazioni sulle dimensioni di un dispositivo. Questa operazione viene restituita dal \_ codice di controllo della capacità di lettura dell'archivio IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Struttura STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401394"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="02679-104">Struttura di capacità di \_ lettura archiviazione \_</span><span class="sxs-lookup"><span data-stu-id="02679-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="02679-105">Contiene informazioni sulle dimensioni di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02679-105">Contains information about the size of a device.</span></span> <span data-ttu-id="02679-106">Questa operazione viene restituita dal codice di controllo della [**\_ capacità di \_ lettura \_ dell'archivio IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .</span><span class="sxs-lookup"><span data-stu-id="02679-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="02679-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02679-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="02679-108">Members</span><span class="sxs-lookup"><span data-stu-id="02679-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="02679-109">**Versione**</span><span class="sxs-lookup"><span data-stu-id="02679-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="02679-110">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="02679-110">The version of this structure.</span></span> <span data-ttu-id="02679-111">Il chiamante deve impostare questo membro su `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="02679-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="02679-112">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="02679-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="02679-113">Dimensione dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="02679-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="02679-114">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="02679-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="02679-115">Numero di byte per blocco.</span><span class="sxs-lookup"><span data-stu-id="02679-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="02679-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="02679-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="02679-117">Numero totale di blocchi sul disco.</span><span class="sxs-lookup"><span data-stu-id="02679-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="02679-118">**DiskLength**</span><span class="sxs-lookup"><span data-stu-id="02679-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="02679-119">Dimensioni del disco in byte.</span><span class="sxs-lookup"><span data-stu-id="02679-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02679-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="02679-120">Remarks</span></span>

<span data-ttu-id="02679-121">Il file di intestazione Ntddstor. h è disponibile nel Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="02679-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="02679-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02679-122">Requirements</span></span>



| <span data-ttu-id="02679-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="02679-123">Requirement</span></span> | <span data-ttu-id="02679-124">Valore</span><span class="sxs-lookup"><span data-stu-id="02679-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02679-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02679-125">Minimum supported client</span></span><br/> | <span data-ttu-id="02679-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02679-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="02679-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02679-127">Minimum supported server</span></span><br/> | <span data-ttu-id="02679-128">Windows Server 2008, Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="02679-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="02679-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02679-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="02679-130"><dt>Ntddstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="02679-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02679-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02679-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02679-132">**\_ \_ capacità lettura archiviazione \_ IOCTL**</span><span class="sxs-lookup"><span data-stu-id="02679-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




