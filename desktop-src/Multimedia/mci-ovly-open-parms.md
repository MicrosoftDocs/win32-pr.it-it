---
title: Struttura MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ struttura OVLY \_ Open \_ parametri di MCI contiene informazioni per il \_ comando di apertura MCI per i dispositivi con sovrimpressione video.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Struttura MCI_OVLY_OPEN_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475095"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="64424-104">\_ \_ Struttura parametri aperta OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="64424-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="64424-105">La **struttura \_ OVLY \_ Open \_ parametri di MCI** contiene informazioni per il comando di [**\_ apertura MCI**](mci-open.md) per i dispositivi con sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="64424-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="64424-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64424-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="64424-107">Members</span><span class="sxs-lookup"><span data-stu-id="64424-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="64424-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="64424-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="64424-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="64424-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="64424-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="64424-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="64424-111">Identificatore restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64424-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="64424-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="64424-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="64424-113">Nome o identificatore costante del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64424-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="64424-114">Il nome del dispositivo viene in genere ottenuto dal registro di sistema o dal file di SYSTEM.INI. Se questo membro è una costante, può essere uno dei valori elencati nei tipi di [dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="64424-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="64424-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="64424-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="64424-116">Nome dell'elemento del dispositivo (in genere un percorso).</span><span class="sxs-lookup"><span data-stu-id="64424-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="64424-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="64424-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="64424-118">Alias del dispositivo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="64424-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="64424-119">**dwStyle**</span><span class="sxs-lookup"><span data-stu-id="64424-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="64424-120">Stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="64424-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="64424-121">**hWndParent**</span><span class="sxs-lookup"><span data-stu-id="64424-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="64424-122">Handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="64424-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64424-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="64424-123">Remarks</span></span>

<span data-ttu-id="64424-124">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="64424-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="64424-125">Se non si usano i membri dati estesi, è possibile usare la struttura [**\_ \_ parametri Open**](mci-open-parms.md) di MCI al posto di **MCI \_ OVLY \_ Open \_ parametri** .</span><span class="sxs-lookup"><span data-stu-id="64424-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="64424-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64424-126">Requirements</span></span>



| <span data-ttu-id="64424-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="64424-127">Requirement</span></span> | <span data-ttu-id="64424-128">Valore</span><span class="sxs-lookup"><span data-stu-id="64424-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64424-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64424-129">Minimum supported client</span></span><br/> | <span data-ttu-id="64424-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64424-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="64424-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64424-131">Minimum supported server</span></span><br/> | <span data-ttu-id="64424-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64424-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64424-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64424-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="64424-134"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="64424-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64424-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64424-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64424-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="64424-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="64424-137">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="64424-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="64424-138">**\_aperto MCI**</span><span class="sxs-lookup"><span data-stu-id="64424-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="64424-139">**\_parametri aperto \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="64424-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="64424-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64424-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

