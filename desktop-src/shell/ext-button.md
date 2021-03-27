---
description: Contiene informazioni su un pulsante aggiunto da una DLL di estensione di file Manager alla barra degli strumenti di gestione file.
title: Struttura EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751015"
---
# <a name="ext_button-structure"></a><span data-ttu-id="dce85-103">\_Struttura pulsante EXT</span><span class="sxs-lookup"><span data-stu-id="dce85-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="dce85-104">Contiene informazioni su un pulsante aggiunto da una DLL di estensione di file Manager alla barra degli strumenti di gestione file.</span><span class="sxs-lookup"><span data-stu-id="dce85-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dce85-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="dce85-106">Members</span><span class="sxs-lookup"><span data-stu-id="dce85-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dce85-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="dce85-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="dce85-108">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="dce85-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dce85-109">Identificatore di comando per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="dce85-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="dce85-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="dce85-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="dce85-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="dce85-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dce85-112">Identificatore della stringa della Guida per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="dce85-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="dce85-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="dce85-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="dce85-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="dce85-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dce85-115">Stile del pulsante.</span><span class="sxs-lookup"><span data-stu-id="dce85-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dce85-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dce85-116">Requirements</span></span>



| <span data-ttu-id="dce85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce85-117">Requirement</span></span> | <span data-ttu-id="dce85-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dce85-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dce85-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce85-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dce85-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dce85-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce85-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dce85-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dce85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce85-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce85-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce85-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dce85-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce85-126">**\_TOOLBARLOAD FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="dce85-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="dce85-127">**\_TOOLBARLOAD FMS**</span><span class="sxs-lookup"><span data-stu-id="dce85-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




