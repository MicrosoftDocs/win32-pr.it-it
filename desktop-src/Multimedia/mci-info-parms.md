---
title: Struttura MCI_INFO_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri info di MCI contiene informazioni per il \_ comando MCI info.
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- Struttura MCI_INFO_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479144"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="a0127-104">\_ \_ Struttura parametri info MCI</span><span class="sxs-lookup"><span data-stu-id="a0127-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="a0127-105">La **struttura \_ \_ parametri info di MCI** contiene informazioni per il comando [**MCI \_ info**](mci-info.md) .</span><span class="sxs-lookup"><span data-stu-id="a0127-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0127-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0127-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="a0127-107">Members</span><span class="sxs-lookup"><span data-stu-id="a0127-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0127-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a0127-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a0127-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="a0127-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a0127-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="a0127-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="a0127-111">Buffer per la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="a0127-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="a0127-112">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="a0127-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="a0127-113">Dimensione, in caratteri, della stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="a0127-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0127-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0127-114">Remarks</span></span>

<span data-ttu-id="a0127-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="a0127-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0127-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0127-116">Requirements</span></span>



| <span data-ttu-id="a0127-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0127-117">Requirement</span></span> | <span data-ttu-id="a0127-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a0127-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0127-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0127-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0127-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0127-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0127-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0127-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0127-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0127-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0127-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0127-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0127-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0127-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0127-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0127-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0127-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a0127-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a0127-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="a0127-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a0127-128">**\_informazioni MCI**</span><span class="sxs-lookup"><span data-stu-id="a0127-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="a0127-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0127-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

