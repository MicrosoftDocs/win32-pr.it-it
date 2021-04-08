---
title: Struttura MPTHREAT_INFOEX_NIS (MpClient. h)
description: Contiene informazioni specifiche di NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- Struttura MPTHREAT_INFOEX_NIS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_NIS
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048312"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="f8335-105">MPTHREAT \_ INFOEX- \_ struttura NIS</span><span class="sxs-lookup"><span data-stu-id="f8335-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="f8335-106">Contiene informazioni specifiche di NIS.</span><span class="sxs-lookup"><span data-stu-id="f8335-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8335-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8335-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="f8335-108">Members</span><span class="sxs-lookup"><span data-stu-id="f8335-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8335-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="f8335-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-110">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="f8335-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="f8335-111">**DestinationIP**</span><span class="sxs-lookup"><span data-stu-id="f8335-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-112">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="f8335-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="f8335-113">**dwSourceport**</span><span class="sxs-lookup"><span data-stu-id="f8335-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f8335-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="f8335-115">**dwDestinationport**</span><span class="sxs-lookup"><span data-stu-id="f8335-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f8335-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="f8335-117">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="f8335-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-118">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="f8335-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="f8335-119">**Collegamento**</span><span class="sxs-lookup"><span data-stu-id="f8335-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="f8335-120">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="f8335-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="f8335-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f8335-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f8335-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8335-122">Requirements</span></span>



| <span data-ttu-id="f8335-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8335-123">Requirement</span></span> | <span data-ttu-id="f8335-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f8335-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8335-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8335-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8335-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f8335-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f8335-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8335-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8335-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f8335-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8335-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8335-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8335-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8335-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





