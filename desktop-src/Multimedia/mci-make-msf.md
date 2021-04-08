---
title: MCI_MAKE_MSF macro (Mciapi. h)
description: La \_ macro MCI make \_ MSF crea un valore di ora in formato minuti/secondi/frame (MSF) compresso dai valori di minuti, secondi e frame specificati.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964913"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="1dab6-104">MCI \_ creare una \_ macro MSF</span><span class="sxs-lookup"><span data-stu-id="1dab6-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="1dab6-105">La macro **MCI \_ make \_ MSF** crea un valore di ora in formato minuti/secondi/frame (MSF) compresso dai valori di minuti, secondi e frame specificati.</span><span class="sxs-lookup"><span data-stu-id="1dab6-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dab6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dab6-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="1dab6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dab6-108">*minuti*</span><span class="sxs-lookup"><span data-stu-id="1dab6-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="1dab6-109">Numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="1dab6-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="1dab6-110">*secondi*</span><span class="sxs-lookup"><span data-stu-id="1dab6-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="1dab6-111">Numero di secondi.</span><span class="sxs-lookup"><span data-stu-id="1dab6-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1dab6-112">*frame*</span><span class="sxs-lookup"><span data-stu-id="1dab6-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="1dab6-113">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="1dab6-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dab6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dab6-114">Return value</span></span>

<span data-ttu-id="1dab6-115">Restituisce l'ora nel formato MSF compresso.</span><span class="sxs-lookup"><span data-stu-id="1dab6-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dab6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dab6-116">Remarks</span></span>

<span data-ttu-id="1dab6-117">L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="1dab6-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="1dab6-118">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="1dab6-118">The most significant byte is unused.</span></span>

<span data-ttu-id="1dab6-119">La macro **MCI \_ make \_ MSF** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="1dab6-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="1dab6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dab6-120">Requirements</span></span>



| <span data-ttu-id="1dab6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dab6-121">Requirement</span></span> | <span data-ttu-id="1dab6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1dab6-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1dab6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dab6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1dab6-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dab6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1dab6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dab6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1dab6-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dab6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1dab6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dab6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dab6-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dab6-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dab6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dab6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dab6-130">MCI</span><span class="sxs-lookup"><span data-stu-id="1dab6-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1dab6-131">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="1dab6-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





