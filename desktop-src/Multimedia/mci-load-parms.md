---
title: Struttura MCI_LOAD_PARMS (mmsystem. h)
description: La \_ \_ struttura parametri Load MCI contiene il nome file da caricare per il \_ comando MCI Load.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Struttura MCI_LOAD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742946"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="98c31-104">\_ \_ Struttura parametri Load MCI</span><span class="sxs-lookup"><span data-stu-id="98c31-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="98c31-105">La **struttura \_ \_ parametri Load MCI** contiene il nome file da caricare per il comando [**MCI \_ Load**](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="98c31-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c31-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98c31-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="98c31-107">Members</span><span class="sxs-lookup"><span data-stu-id="98c31-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="98c31-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="98c31-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="98c31-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="98c31-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="98c31-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="98c31-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="98c31-111">Nome del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="98c31-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98c31-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="98c31-112">Remarks</span></span>

<span data-ttu-id="98c31-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="98c31-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c31-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98c31-114">Requirements</span></span>



| <span data-ttu-id="98c31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c31-115">Requirement</span></span> | <span data-ttu-id="98c31-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98c31-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98c31-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98c31-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98c31-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98c31-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="98c31-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98c31-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98c31-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98c31-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98c31-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98c31-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c31-122"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c31-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c31-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98c31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c31-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="98c31-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98c31-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="98c31-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="98c31-126">**\_carico MCI**</span><span class="sxs-lookup"><span data-stu-id="98c31-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="98c31-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="98c31-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

