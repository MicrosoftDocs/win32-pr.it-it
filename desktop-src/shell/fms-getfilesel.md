---
description: Contiene informazioni su un file selezionato nella finestra attiva di File Manager (la finestra della directory o la finestra Risultati ricerca).
title: FMS_GETFILESEL struttura (Wfext.h)
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
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842222"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="cd601-103">Struttura \_ FMS GETFILESEL</span><span class="sxs-lookup"><span data-stu-id="cd601-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="cd601-104">Contiene informazioni su un file selezionato nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="cd601-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd601-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd601-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="cd601-106">Members</span><span class="sxs-lookup"><span data-stu-id="cd601-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd601-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="cd601-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="cd601-108">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="cd601-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="cd601-109">Ora e data di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="cd601-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="cd601-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="cd601-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="cd601-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd601-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd601-112">Dimensione, in byte, del file.</span><span class="sxs-lookup"><span data-stu-id="cd601-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="cd601-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="cd601-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="cd601-114">Tipo: **BYTE**</span><span class="sxs-lookup"><span data-stu-id="cd601-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="cd601-115">Attributi del file.</span><span class="sxs-lookup"><span data-stu-id="cd601-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="cd601-116">**Szname**</span><span class="sxs-lookup"><span data-stu-id="cd601-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="cd601-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="cd601-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="cd601-118">Percorso completo con terminazione Null e nome file del file selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd601-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd601-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd601-119">Requirements</span></span>



| <span data-ttu-id="cd601-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd601-120">Requirement</span></span> | <span data-ttu-id="cd601-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cd601-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd601-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd601-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd601-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd601-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cd601-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd601-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd601-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd601-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cd601-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd601-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd601-127"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="cd601-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd601-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd601-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd601-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="cd601-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




