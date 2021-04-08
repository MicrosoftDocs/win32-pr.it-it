---
title: Struttura MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: La \_ struttura GETDEVCAPS \_ parametri di MCI contiene informazioni sulle funzionalità del dispositivo per il \_ comando MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Struttura MCI_GETDEVCAPS_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048057"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="83c1e-104">\_Struttura parametri GETDEVCAPS di MCI \_</span><span class="sxs-lookup"><span data-stu-id="83c1e-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="83c1e-105">La **struttura \_ GETDEVCAPS \_ parametri di MCI** contiene informazioni sulle funzionalità del dispositivo per il comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="83c1e-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c1e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83c1e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="83c1e-107">Members</span><span class="sxs-lookup"><span data-stu-id="83c1e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="83c1e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="83c1e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="83c1e-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="83c1e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="83c1e-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="83c1e-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="83c1e-111">Contiene informazioni sull'uscita.</span><span class="sxs-lookup"><span data-stu-id="83c1e-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="83c1e-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="83c1e-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="83c1e-113">Funzionalità sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="83c1e-113">Capability being queried.</span></span> <span data-ttu-id="83c1e-114">Questo membro può essere una delle costanti elencate nel materiale di riferimento per il comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="83c1e-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83c1e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="83c1e-115">Remarks</span></span>

<span data-ttu-id="83c1e-116">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="83c1e-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c1e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83c1e-117">Requirements</span></span>



| <span data-ttu-id="83c1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c1e-118">Requirement</span></span> | <span data-ttu-id="83c1e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="83c1e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83c1e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c1e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83c1e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83c1e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="83c1e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83c1e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83c1e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83c1e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="83c1e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83c1e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c1e-125"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c1e-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c1e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83c1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c1e-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="83c1e-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="83c1e-128">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="83c1e-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="83c1e-129">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="83c1e-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="83c1e-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83c1e-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

