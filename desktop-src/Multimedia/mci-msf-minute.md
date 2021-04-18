---
title: MCI_MSF_MINUTE macro (Mciapi. h)
description: La \_ macro del \_ momento MSF di MCI Recupera il componente minuti da un parametro contenente le informazioni relative a minuti/secondi/frame (MSF) compressi.
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302629"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="b5156-104">\_Macro del minuto MSF di MCI \_</span><span class="sxs-lookup"><span data-stu-id="b5156-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="b5156-105">La macro del **\_ \_ momento MSF di MCI** Recupera il componente minuti da un parametro contenente le informazioni relative a minuti/secondi/frame (MSF) compressi.</span><span class="sxs-lookup"><span data-stu-id="b5156-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5156-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5156-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="b5156-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5156-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5156-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="b5156-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="b5156-109">Tempo in formato MSF.</span><span class="sxs-lookup"><span data-stu-id="b5156-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5156-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5156-110">Return value</span></span>

<span data-ttu-id="b5156-111">Restituisce il componente minuti delle informazioni MSF specificate.</span><span class="sxs-lookup"><span data-stu-id="b5156-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5156-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5156-112">Remarks</span></span>

<span data-ttu-id="b5156-113">L'ora nel formato MSF è espressa come valore **DWORD** con il byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il successivo byte meno significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="b5156-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="b5156-114">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="b5156-114">The most significant byte is unused.</span></span>

<span data-ttu-id="b5156-115">La macro del **\_ \_ minuto MSF di MCI** è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="b5156-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="b5156-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5156-116">Requirements</span></span>



| <span data-ttu-id="b5156-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5156-117">Requirement</span></span> | <span data-ttu-id="b5156-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b5156-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5156-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5156-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5156-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5156-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b5156-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5156-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5156-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5156-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5156-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5156-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5156-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5156-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5156-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5156-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5156-126">MCI</span><span class="sxs-lookup"><span data-stu-id="b5156-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b5156-127">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="b5156-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





