---
title: Struttura MCI_VCR_STATUS_PARMS (VCR. h)
description: La \_ \_ struttura parametri di stato VCR MCI contiene i \_ parametri per il \_ comando di stato MCI per i registratori di cassette video.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- Struttura MCI_VCR_STATUS_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963827"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="81134-104">\_ \_ Struttura parametri stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="81134-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="81134-105">La **struttura \_ \_ \_ parametri di stato VCR MCI** contiene i parametri per il comando di [**\_ stato MCI**](mci-status.md) per i registratori di cassette video.</span><span class="sxs-lookup"><span data-stu-id="81134-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="81134-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81134-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="81134-107">Members</span><span class="sxs-lookup"><span data-stu-id="81134-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="81134-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="81134-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="81134-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="81134-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="81134-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="81134-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="81134-111">Valore restituito dal comando [**MCI \_ status**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="81134-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="81134-112">Il valore restituito varia a seconda dell'indagine del comando.</span><span class="sxs-lookup"><span data-stu-id="81134-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="81134-113">Per ulteriori informazioni, vedere la descrizione del comando [**MCI \_ status**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="81134-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="81134-114">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="81134-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="81134-115">Tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="81134-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="81134-116">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="81134-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="81134-117">Traccia audio o video che archivia le informazioni durante la registrazione successiva.</span><span class="sxs-lookup"><span data-stu-id="81134-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="81134-118">Questo membro viene usato per restituire informazioni quando il comando di [**\_ stato MCI**](mci-status-parms.md) chiede lo stato di registrazione video o audio.</span><span class="sxs-lookup"><span data-stu-id="81134-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="81134-119">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="81134-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="81134-120">Tuner logico a cui è associato il canale corrente.</span><span class="sxs-lookup"><span data-stu-id="81134-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="81134-121">Questo membro viene usato per restituire informazioni quando il comando di [**\_ stato MCI**](mci-status.md) chiede informazioni sul numero di canale corrente.</span><span class="sxs-lookup"><span data-stu-id="81134-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81134-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="81134-122">Remarks</span></span>

<span data-ttu-id="81134-123">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="81134-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="81134-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81134-124">Requirements</span></span>



| <span data-ttu-id="81134-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="81134-125">Requirement</span></span> | <span data-ttu-id="81134-126">Valore</span><span class="sxs-lookup"><span data-stu-id="81134-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="81134-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81134-127">Minimum supported client</span></span><br/> | <span data-ttu-id="81134-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81134-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="81134-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81134-129">Minimum supported server</span></span><br/> | <span data-ttu-id="81134-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81134-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="81134-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81134-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="81134-132"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="81134-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81134-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81134-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81134-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="81134-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="81134-135">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="81134-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="81134-136">**\_stato MCI**</span><span class="sxs-lookup"><span data-stu-id="81134-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="81134-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81134-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

