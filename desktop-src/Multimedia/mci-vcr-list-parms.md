---
title: Struttura MCI_VCR_LIST_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ List \_ contiene i parametri per il \_ comando elenco MCI per i registratori di nastri video.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- Struttura MCI_VCR_LIST_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341153"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="185b4-104">\_ \_ Struttura parametri elenco VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="185b4-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="185b4-105">La struttura **parametri di MCI \_ VCR \_ List \_** contiene i parametri per il comando [**\_ elenco MCI**](mci-list.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="185b4-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="185b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="185b4-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="185b4-107">Members</span><span class="sxs-lookup"><span data-stu-id="185b4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="185b4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="185b4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="185b4-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="185b4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="185b4-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="185b4-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="185b4-111">Buffer per le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="185b4-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="185b4-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="185b4-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="185b4-113">Numero di input video o audio del videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="185b4-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="185b4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="185b4-114">Remarks</span></span>

<span data-ttu-id="185b4-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="185b4-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="185b4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="185b4-116">Requirements</span></span>



| <span data-ttu-id="185b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="185b4-117">Requirement</span></span> | <span data-ttu-id="185b4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="185b4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="185b4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="185b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="185b4-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="185b4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="185b4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="185b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="185b4-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="185b4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="185b4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="185b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="185b4-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="185b4-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185b4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="185b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185b4-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="185b4-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="185b4-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="185b4-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="185b4-128">**\_elenco MCI**</span><span class="sxs-lookup"><span data-stu-id="185b4-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="185b4-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="185b4-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

