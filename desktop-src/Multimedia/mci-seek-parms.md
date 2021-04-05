---
title: Struttura MCI_SEEK_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri Seek di MCI contiene informazioni sul posizionamento per il \_ comando di ricerca MCI.
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- Struttura MCI_SEEK_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740487"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="07862-104">\_Struttura parametri Seek di MCI \_</span><span class="sxs-lookup"><span data-stu-id="07862-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="07862-105">La **struttura \_ \_ parametri Seek di MCI** contiene informazioni sul posizionamento per il comando di [**\_ ricerca MCI**](mci-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="07862-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="07862-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07862-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="07862-107">Members</span><span class="sxs-lookup"><span data-stu-id="07862-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07862-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="07862-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="07862-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="07862-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="07862-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="07862-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="07862-111">Posizione in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="07862-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07862-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="07862-112">Remarks</span></span>

<span data-ttu-id="07862-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="07862-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="07862-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07862-114">Requirements</span></span>



| <span data-ttu-id="07862-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07862-115">Requirement</span></span> | <span data-ttu-id="07862-116">Valore</span><span class="sxs-lookup"><span data-stu-id="07862-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07862-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07862-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07862-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07862-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07862-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07862-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07862-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07862-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07862-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07862-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07862-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="07862-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07862-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07862-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07862-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="07862-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="07862-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="07862-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="07862-126">**\_ricerca MCI**</span><span class="sxs-lookup"><span data-stu-id="07862-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="07862-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07862-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

