---
description: Contiene informazioni su un pulsante aggiunto da una DLL di estensione di File Manager alla barra degli strumenti di File Manager.
title: EXT_BUTTON struttura (Wfext.h)
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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843152"
---
# <a name="ext_button-structure"></a><span data-ttu-id="77636-103">Struttura EXT \_ BUTTON</span><span class="sxs-lookup"><span data-stu-id="77636-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="77636-104">Contiene informazioni su un pulsante aggiunto da una DLL di estensione di File Manager alla barra degli strumenti di File Manager.</span><span class="sxs-lookup"><span data-stu-id="77636-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="77636-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77636-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="77636-106">Members</span><span class="sxs-lookup"><span data-stu-id="77636-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="77636-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="77636-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="77636-108">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="77636-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="77636-109">Identificatore di comando per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="77636-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="77636-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="77636-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="77636-111">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="77636-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="77636-112">Identificatore della stringa della Guida per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="77636-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="77636-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="77636-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="77636-114">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="77636-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="77636-115">Stile del pulsante.</span><span class="sxs-lookup"><span data-stu-id="77636-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77636-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77636-116">Requirements</span></span>



| <span data-ttu-id="77636-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77636-117">Requirement</span></span> | <span data-ttu-id="77636-118">Valore</span><span class="sxs-lookup"><span data-stu-id="77636-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77636-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77636-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77636-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="77636-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="77636-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77636-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77636-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="77636-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="77636-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77636-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77636-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="77636-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77636-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77636-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77636-126">**BARRA DEGLI STRUMENTI \_ FMEVENTLOAD**</span><span class="sxs-lookup"><span data-stu-id="77636-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="77636-127">**BARRA DEGLI STRUMENTI \_ FMSCARICA**</span><span class="sxs-lookup"><span data-stu-id="77636-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




