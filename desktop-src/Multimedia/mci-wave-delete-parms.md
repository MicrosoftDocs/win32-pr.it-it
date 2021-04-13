---
title: Struttura MCI_WAVE_DELETE_PARMS (Mciapi. h)
description: La \_ \_ \_ struttura parametri per l'eliminazione di MCI Wave contiene informazioni sulla posizione per il \_ comando MCI Delete per i dispositivi audio waveform.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Struttura MCI_WAVE_DELETE_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475683"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="b52bb-104">\_ \_ Struttura parametri Delete Wave MCI \_</span><span class="sxs-lookup"><span data-stu-id="b52bb-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="b52bb-105">La **struttura \_ \_ \_ parametri** per l'eliminazione di MCI Wave contiene informazioni sulla posizione per il comando [**MCI \_ Delete**](mci-delete.md) per i dispositivi audio waveform.</span><span class="sxs-lookup"><span data-stu-id="b52bb-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52bb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b52bb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="b52bb-107">Members</span><span class="sxs-lookup"><span data-stu-id="b52bb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b52bb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b52bb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b52bb-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="b52bb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b52bb-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="b52bb-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="b52bb-111">Posizione da cui eliminare.</span><span class="sxs-lookup"><span data-stu-id="b52bb-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="b52bb-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="b52bb-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="b52bb-113">Posizione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b52bb-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b52bb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b52bb-114">Remarks</span></span>

<span data-ttu-id="b52bb-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="b52bb-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52bb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b52bb-116">Requirements</span></span>



| <span data-ttu-id="b52bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52bb-117">Requirement</span></span> | <span data-ttu-id="b52bb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b52bb-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b52bb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b52bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b52bb-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b52bb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b52bb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b52bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b52bb-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b52bb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b52bb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b52bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52bb-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52bb-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52bb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b52bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52bb-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b52bb-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b52bb-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="b52bb-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b52bb-128">**eliminazione di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b52bb-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="b52bb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b52bb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

