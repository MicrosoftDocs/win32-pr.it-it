---
description: Contiene dati che descrivono un esperto all'avvio.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Struttura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966479"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="bfbd0-103">Struttura EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="bfbd0-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="bfbd0-104">La struttura **EXPERTSTARTUPINFO** contiene dati che descrivono un esperto all'avvio.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfbd0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfbd0-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="bfbd0-106">Members</span><span class="sxs-lookup"><span data-stu-id="bfbd0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfbd0-107">**Flag**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-108">Flag che descrivono l'esperto.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-109">**hCapture**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-110">Handle per un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-111">**szCaptureFile**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-112">Nome del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-113">**dwFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-114">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-115">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-116">Handle per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-117">**lpPropertyInst**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-118">Puntatore a una struttura [**PROPERTYINST**](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbd0-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-119">**sBitfield**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfbd0-120">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-121">Utilizzato solo se il membro **dataqualifier** della struttura [**PROPERTYINST**](propertyinst.md) è impostato su propa \_ \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd0-122">**bOn**</span><span class="sxs-lookup"><span data-stu-id="bfbd0-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="bfbd0-123">Utilizzato solo se il membro **dataqualifier** della struttura [**PROPERTYINST**](propertyinst.md) è impostato su propa \_ \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="bfbd0-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfbd0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfbd0-124">Requirements</span></span>



| <span data-ttu-id="bfbd0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfbd0-125">Requirement</span></span> | <span data-ttu-id="bfbd0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bfbd0-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbd0-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfbd0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bfbd0-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfbd0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bfbd0-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfbd0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bfbd0-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfbd0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bfbd0-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfbd0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfbd0-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfbd0-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




