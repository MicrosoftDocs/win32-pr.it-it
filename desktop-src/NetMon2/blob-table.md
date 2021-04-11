---
description: Contiene una matrice di BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Struttura BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227387"
---
# <a name="blob_table-structure"></a><span data-ttu-id="abad9-103">\_Struttura della tabella BLOB</span><span class="sxs-lookup"><span data-stu-id="abad9-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="abad9-104">La struttura della **\_ tabella BLOB** contiene una matrice di BLOB.</span><span class="sxs-lookup"><span data-stu-id="abad9-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="abad9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abad9-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="abad9-106">Members</span><span class="sxs-lookup"><span data-stu-id="abad9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="abad9-107">**dwNumBlobs**</span><span class="sxs-lookup"><span data-stu-id="abad9-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="abad9-108">Indica che molti BLOB seguono.</span><span class="sxs-lookup"><span data-stu-id="abad9-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="abad9-109">**hBlobs**</span><span class="sxs-lookup"><span data-stu-id="abad9-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="abad9-110">Handle per la matrice BLOB.</span><span class="sxs-lookup"><span data-stu-id="abad9-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abad9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abad9-111">Requirements</span></span>



| <span data-ttu-id="abad9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="abad9-112">Requirement</span></span> | <span data-ttu-id="abad9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="abad9-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="abad9-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abad9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="abad9-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="abad9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="abad9-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abad9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="abad9-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="abad9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="abad9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abad9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="abad9-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="abad9-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




