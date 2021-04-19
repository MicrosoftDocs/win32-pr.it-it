---
description: Struttura utilizzata dalla funzione SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Struttura PPROTECT_FILE_ENTRY (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312702"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="dad7f-103">\_Struttura di \_ immissione file PPROTECT</span><span class="sxs-lookup"><span data-stu-id="dad7f-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="dad7f-104">\[Questa struttura è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="dad7f-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dad7f-105">Il supporto per questa struttura è stato rimosso in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dad7f-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="dad7f-106">Usare invece le funzioni supportate elencate in [WRP Functions](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="dad7f-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="dad7f-107">Struttura utilizzata dalla funzione [**SfcGetFiles**](sfcgetfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="dad7f-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad7f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dad7f-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="dad7f-109">Members</span><span class="sxs-lookup"><span data-stu-id="dad7f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dad7f-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="dad7f-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="dad7f-111">Puntatore a un valore stringa contenente il nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="dad7f-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="dad7f-112">Questo valore sarà **null** se il file non viene rinominato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dad7f-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="dad7f-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="dad7f-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="dad7f-114">Puntatore a un valore stringa contenente il nome file di destinazione più il percorso completo del file.</span><span class="sxs-lookup"><span data-stu-id="dad7f-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="dad7f-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="dad7f-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="dad7f-116">Puntatore a un valore stringa contenente il nome del file INF che fornisce informazioni sul layout.</span><span class="sxs-lookup"><span data-stu-id="dad7f-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="dad7f-117">Questo parametro può essere **null** quando si usa il layout predefinito.</span><span class="sxs-lookup"><span data-stu-id="dad7f-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dad7f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dad7f-118">Requirements</span></span>



| <span data-ttu-id="dad7f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad7f-119">Requirement</span></span> | <span data-ttu-id="dad7f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dad7f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dad7f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dad7f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dad7f-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dad7f-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dad7f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dad7f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dad7f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dad7f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dad7f-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dad7f-125">End of client support</span></span><br/>    | <span data-ttu-id="dad7f-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dad7f-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="dad7f-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="dad7f-127">End of server support</span></span><br/>    | <span data-ttu-id="dad7f-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dad7f-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="dad7f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dad7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad7f-130"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad7f-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad7f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dad7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad7f-132">**SfcGetFiles**</span><span class="sxs-lookup"><span data-stu-id="dad7f-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




