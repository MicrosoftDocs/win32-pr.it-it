---
description: Contiene informazioni su un file selezionato nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Struttura FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966396"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="84841-103">\_Struttura GETFILESEL FMS</span><span class="sxs-lookup"><span data-stu-id="84841-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="84841-104">Contiene informazioni su un file selezionato nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="84841-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="84841-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84841-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="84841-106">Members</span><span class="sxs-lookup"><span data-stu-id="84841-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="84841-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="84841-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="84841-108">Tipo: **FILEtime**</span><span class="sxs-lookup"><span data-stu-id="84841-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="84841-109">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="84841-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="84841-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="84841-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="84841-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84841-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84841-112">Dimensione, in byte, del file.</span><span class="sxs-lookup"><span data-stu-id="84841-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="84841-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="84841-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="84841-114">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="84841-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="84841-115">Attributi del file.</span><span class="sxs-lookup"><span data-stu-id="84841-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="84841-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="84841-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="84841-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="84841-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="84841-118">Il percorso completo con terminazione null e il nome del file selezionato.</span><span class="sxs-lookup"><span data-stu-id="84841-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84841-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84841-119">Requirements</span></span>



| <span data-ttu-id="84841-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84841-120">Requirement</span></span> | <span data-ttu-id="84841-121">Valore</span><span class="sxs-lookup"><span data-stu-id="84841-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84841-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84841-122">Minimum supported client</span></span><br/> | <span data-ttu-id="84841-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="84841-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="84841-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84841-124">Minimum supported server</span></span><br/> | <span data-ttu-id="84841-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="84841-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84841-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84841-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="84841-127"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="84841-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84841-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84841-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84841-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="84841-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




