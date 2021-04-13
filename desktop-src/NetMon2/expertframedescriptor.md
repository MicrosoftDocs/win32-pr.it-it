---
description: La struttura EXPERTFRAMEDESCRIPTOR contiene informazioni su un frame. Quando l'esperto chiama la funzione ExpertGetFrame correttamente, Network Monitor passa nuovamente la struttura EXPERTFRAMEDESCRIPTOR all'esperto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Struttura EXPERTFRAMEDESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484340"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="43fec-104">Struttura EXPERTFRAMEDESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="43fec-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="43fec-105">La struttura **EXPERTFRAMEDESCRIPTOR** contiene informazioni su un frame.</span><span class="sxs-lookup"><span data-stu-id="43fec-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="43fec-106">Quando l'esperto chiama la funzione [**ExpertGetFrame**](expertgetframe.md) correttamente, network monitor passa nuovamente la struttura **EXPERTFRAMEDESCRIPTOR** all'esperto.</span><span class="sxs-lookup"><span data-stu-id="43fec-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43fec-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="43fec-108">Members</span><span class="sxs-lookup"><span data-stu-id="43fec-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="43fec-109">**NumeroFrame**</span><span class="sxs-lookup"><span data-stu-id="43fec-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="43fec-110">Numero di un frame specificato.</span><span class="sxs-lookup"><span data-stu-id="43fec-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="43fec-111">**hFrame**</span><span class="sxs-lookup"><span data-stu-id="43fec-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="43fec-112">Handle per un frame.</span><span class="sxs-lookup"><span data-stu-id="43fec-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="43fec-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="43fec-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="43fec-114">Puntatore a un frame non elaborato.</span><span class="sxs-lookup"><span data-stu-id="43fec-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="43fec-115">**lpRecognizeDataTable**</span><span class="sxs-lookup"><span data-stu-id="43fec-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="43fec-116">Tabella che indica dove ogni parser identifica l'inizio dei dati.</span><span class="sxs-lookup"><span data-stu-id="43fec-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="43fec-117">**lpPropertyTable**</span><span class="sxs-lookup"><span data-stu-id="43fec-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="43fec-118">Tabella delle proprietà del frame identificate dal parser.</span><span class="sxs-lookup"><span data-stu-id="43fec-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43fec-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="43fec-119">Remarks</span></span>

<span data-ttu-id="43fec-120">Se l'esperto specifica le \_ proprietà di associazione dei flag \_ quando si chiama [**ExpertGetFrame**](expertgetframe.md), il membro **szPropertyText** in ogni struttura [**PROPERTYINST**](propertyinst.md) è **null**.</span><span class="sxs-lookup"><span data-stu-id="43fec-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="43fec-121">Se l'esperto non specifica le proprietà di associazione dei flag \_ \_ quando chiama la funzione [**ExpertGetFrame**](expertgetframe.md) , il membro **lpPropertyTable** è **null** alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="43fec-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="43fec-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43fec-122">Requirements</span></span>



| <span data-ttu-id="43fec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fec-123">Requirement</span></span> | <span data-ttu-id="43fec-124">Valore</span><span class="sxs-lookup"><span data-stu-id="43fec-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43fec-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="43fec-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43fec-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="43fec-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="43fec-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43fec-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43fec-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43fec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="43fec-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fec-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




