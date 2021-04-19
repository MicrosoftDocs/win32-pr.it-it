---
description: Definisce il comportamento di richiesta dell'archivio protetto ogni volta che viene visualizzata un'interfaccia utente.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Struttura PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328036"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="88ad7-103">\_Struttura PROMPTINFO PST</span><span class="sxs-lookup"><span data-stu-id="88ad7-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="88ad7-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88ad7-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="88ad7-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="88ad7-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="88ad7-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="88ad7-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="88ad7-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="88ad7-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="88ad7-108">Definisce il comportamento di richiesta dell'archivio protetto ogni volta che viene visualizzata un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="88ad7-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ad7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ad7-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="88ad7-110">Members</span><span class="sxs-lookup"><span data-stu-id="88ad7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="88ad7-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="88ad7-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="88ad7-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="88ad7-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="88ad7-113">**dwPromptFlags**</span><span class="sxs-lookup"><span data-stu-id="88ad7-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="88ad7-114">Questo flag viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="88ad7-114">This flag is ignored.</span></span>



| <span data-ttu-id="88ad7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="88ad7-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="88ad7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="88ad7-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="88ad7-117"><dt>**Pst \_ PF \_ \_ Mostra sempre**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="88ad7-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="88ad7-118">Richiede che il provider visualizzi la finestra di dialogo di richiesta all'utente anche se non è necessaria per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="88ad7-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="88ad7-119"><dt>**Pst \_ PF \_ non \_ Mostra mai**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="88ad7-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="88ad7-120">Non visualizzare la finestra di dialogo di richiesta all'utente.</span><span class="sxs-lookup"><span data-stu-id="88ad7-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="88ad7-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="88ad7-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="88ad7-122">Handle per la finestra padre dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="88ad7-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="88ad7-123">Il membro **hwndApp** determina la posizione in cui viene visualizzata l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="88ad7-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="88ad7-124">Se viene passato **null** , il desktop viene considerato la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="88ad7-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="88ad7-125">**szPrompt**</span><span class="sxs-lookup"><span data-stu-id="88ad7-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="88ad7-126">Stringa di richiesta.</span><span class="sxs-lookup"><span data-stu-id="88ad7-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88ad7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88ad7-127">Requirements</span></span>



| <span data-ttu-id="88ad7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ad7-128">Requirement</span></span> | <span data-ttu-id="88ad7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="88ad7-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88ad7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88ad7-130">Header</span></span><br/> | <dl> <span data-ttu-id="88ad7-131"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="88ad7-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ad7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88ad7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ad7-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="88ad7-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="88ad7-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="88ad7-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="88ad7-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="88ad7-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="88ad7-136">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="88ad7-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
