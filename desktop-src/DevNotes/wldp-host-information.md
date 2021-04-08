---
description: Struttura che identifica l'host e il file di origine da valutare.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Struttura WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049097"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="afff9-103">\_ \_ Struttura delle informazioni sull'host WLDP</span><span class="sxs-lookup"><span data-stu-id="afff9-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="afff9-104">Struttura che identifica l'host e il file di origine da valutare.</span><span class="sxs-lookup"><span data-stu-id="afff9-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="afff9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afff9-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="afff9-106">Members</span><span class="sxs-lookup"><span data-stu-id="afff9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="afff9-107">**dwRevision**</span><span class="sxs-lookup"><span data-stu-id="afff9-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="afff9-108">Deve essere **la \_ \_ \_ revisione delle informazioni sull'host WLDP**.</span><span class="sxs-lookup"><span data-stu-id="afff9-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="afff9-109">**dwHostId**</span><span class="sxs-lookup"><span data-stu-id="afff9-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="afff9-110">Valore di enumerazione [**dell' \_ \_ ID host WLDP**](wldp-host-id.md) che descrive l'ID host.</span><span class="sxs-lookup"><span data-stu-id="afff9-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="afff9-111">**szSource**</span><span class="sxs-lookup"><span data-stu-id="afff9-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="afff9-112">Percorso completo e nome di script con l'estensione.</span><span class="sxs-lookup"><span data-stu-id="afff9-112">Full path and script name with the extension.</span></span> <span data-ttu-id="afff9-113">NULL per **l' \_ ID host WLDP \_ \_ globale** o l'esecuzione di script manuale.</span><span class="sxs-lookup"><span data-stu-id="afff9-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="afff9-114">**hSource**</span><span class="sxs-lookup"><span data-stu-id="afff9-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="afff9-115">Oltre al nome, il chiamante può specificare un handle per il file utilizzato per la convalida.</span><span class="sxs-lookup"><span data-stu-id="afff9-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afff9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afff9-116">Requirements</span></span>



| <span data-ttu-id="afff9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="afff9-117">Requirement</span></span> | <span data-ttu-id="afff9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="afff9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="afff9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afff9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="afff9-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="afff9-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afff9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afff9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="afff9-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="afff9-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="afff9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afff9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="afff9-124"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="afff9-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




