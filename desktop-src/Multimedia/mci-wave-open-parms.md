---
title: Struttura MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: La \_ \_ \_ struttura parametri Wave Open di MCI contiene informazioni per il \_ comando di apertura di MCI per i dispositivi audio waveform.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Struttura MCI_WAVE_OPEN_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302028"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="edb31-104">\_ \_ Struttura parametri Wave Open di MCI \_</span><span class="sxs-lookup"><span data-stu-id="edb31-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="edb31-105">La **struttura \_ \_ \_ parametri Wave Open di MCI** contiene informazioni per il comando di [**\_ apertura di MCI**](mci-open.md) per i dispositivi audio waveform.</span><span class="sxs-lookup"><span data-stu-id="edb31-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb31-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edb31-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="edb31-107">Members</span><span class="sxs-lookup"><span data-stu-id="edb31-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="edb31-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="edb31-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="edb31-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="edb31-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="edb31-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-111">Identificatore restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="edb31-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="edb31-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="edb31-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-113">Nome o identificatore costante del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edb31-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="edb31-114">Il nome del dispositivo viene in genere ottenuto dal registro di sistema o dal file di SYSTEM.INI. Questo membro può essere uno dei valori elencati in [tipi di dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="edb31-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="edb31-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="edb31-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-116">Nome dell'elemento del dispositivo (in genere un percorso).</span><span class="sxs-lookup"><span data-stu-id="edb31-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="edb31-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="edb31-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-118">Alias del dispositivo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edb31-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="edb31-119">**dwBufferSeconds**</span><span class="sxs-lookup"><span data-stu-id="edb31-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="edb31-120">Lunghezza del buffer, in secondi.</span><span class="sxs-lookup"><span data-stu-id="edb31-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edb31-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="edb31-121">Remarks</span></span>

<span data-ttu-id="edb31-122">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="edb31-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="edb31-123">Se non si usano i membri dati estesi, è possibile usare la struttura [**\_ \_ parametri Open**](mci-open-parms.md) di MCI invece di **MCI \_ Wave \_ Open \_ parametri** .</span><span class="sxs-lookup"><span data-stu-id="edb31-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb31-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edb31-124">Requirements</span></span>



| <span data-ttu-id="edb31-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb31-125">Requirement</span></span> | <span data-ttu-id="edb31-126">Valore</span><span class="sxs-lookup"><span data-stu-id="edb31-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edb31-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edb31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="edb31-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edb31-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="edb31-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edb31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="edb31-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edb31-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="edb31-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edb31-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb31-132"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb31-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb31-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edb31-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb31-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="edb31-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="edb31-135">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="edb31-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="edb31-136">**\_aperto MCI**</span><span class="sxs-lookup"><span data-stu-id="edb31-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="edb31-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="edb31-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="edb31-138">**\_parametri aperto \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="edb31-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

