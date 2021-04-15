---
title: Messaggio MMIOM_RENAME (mmsystem. h)
description: Il \_ messaggio MMIOM Rename viene inviato a una routine di i/O dalla funzione mmioRename per richiedere che il file specificato venga rinominato.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478455"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="613be-104">MMIOM \_ Rinomina messaggio</span><span class="sxs-lookup"><span data-stu-id="613be-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="613be-105">Il messaggio **MMIOM \_ Rename** viene inviato a una routine di i/O dalla funzione [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) per richiedere che il file specificato venga rinominato.</span><span class="sxs-lookup"><span data-stu-id="613be-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="613be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="613be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613be-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span><span class="sxs-lookup"><span data-stu-id="613be-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="613be-108">Puntatore a una stringa contenente il nome del file da rinominare.</span><span class="sxs-lookup"><span data-stu-id="613be-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="613be-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span><span class="sxs-lookup"><span data-stu-id="613be-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="613be-110">Puntatore a una stringa che contiene il nuovo nome file.</span><span class="sxs-lookup"><span data-stu-id="613be-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613be-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="613be-111">Return Value</span></span>

<span data-ttu-id="613be-112">Se il file viene rinominato correttamente, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="613be-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="613be-113">Se il file specificato non è stato trovato, il valore restituito è MMIOERR \_ FileNotFound.</span><span class="sxs-lookup"><span data-stu-id="613be-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="613be-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="613be-114">Requirements</span></span>



| <span data-ttu-id="613be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="613be-115">Requirement</span></span> | <span data-ttu-id="613be-116">Valore</span><span class="sxs-lookup"><span data-stu-id="613be-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613be-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="613be-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613be-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="613be-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="613be-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613be-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="613be-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="613be-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="613be-122"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="613be-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

