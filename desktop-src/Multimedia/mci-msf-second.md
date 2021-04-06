---
title: MCI_MSF_SECOND macro (Mciapi. h)
description: La \_ seconda macro del MCI MSF \_ Recupera il componente secondi da un parametro contenente le informazioni sui minuti/secondi/frame (MSF) compressi.
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873981"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="ab6ef-104">\_ \_ Seconda macro del MCI MSF</span><span class="sxs-lookup"><span data-stu-id="ab6ef-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="ab6ef-105">La **\_ \_ seconda macro del MCI MSF** Recupera il componente secondi da un parametro contenente le informazioni sui minuti/secondi/frame (MSF) compressi.</span><span class="sxs-lookup"><span data-stu-id="ab6ef-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab6ef-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="ab6ef-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab6ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6ef-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="ab6ef-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="ab6ef-109">Tempo in formato MSF.</span><span class="sxs-lookup"><span data-stu-id="ab6ef-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6ef-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab6ef-110">Return value</span></span>

<span data-ttu-id="ab6ef-111">Restituisce il componente relativo ai secondi delle informazioni MSF specificate.</span><span class="sxs-lookup"><span data-stu-id="ab6ef-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6ef-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab6ef-112">Remarks</span></span>

<span data-ttu-id="ab6ef-113">L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="ab6ef-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="ab6ef-114">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="ab6ef-114">The most significant byte is unused.</span></span>

<span data-ttu-id="ab6ef-115">La **\_ \_ seconda** macro del MSF di MCI è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="ab6ef-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="ab6ef-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab6ef-116">Requirements</span></span>



| <span data-ttu-id="ab6ef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6ef-117">Requirement</span></span> | <span data-ttu-id="ab6ef-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ab6ef-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6ef-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab6ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6ef-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab6ef-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ab6ef-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab6ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6ef-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab6ef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab6ef-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab6ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6ef-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6ef-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6ef-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab6ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6ef-126">MCI</span><span class="sxs-lookup"><span data-stu-id="ab6ef-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ab6ef-127">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="ab6ef-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





