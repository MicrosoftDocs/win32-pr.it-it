---
description: Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando Annulla eliminazione dal menu file.
title: Puntatore a funzione FM_UNDELETE_PROC (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233561"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="be37f-103">\_Puntatore alla funzione di annullamento dell'eliminazione FM \_</span><span class="sxs-lookup"><span data-stu-id="be37f-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="be37f-104">Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando **Annulla eliminazione** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="be37f-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="be37f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be37f-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="be37f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be37f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be37f-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="be37f-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="be37f-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="be37f-108">Type: **HWND**</span></span>

<span data-ttu-id="be37f-109">Handle della finestra per file Manager.</span><span class="sxs-lookup"><span data-stu-id="be37f-109">The window handle to File Manager.</span></span> <span data-ttu-id="be37f-110">Una DLL di annullamento dell'eliminazione deve utilizzare questo handle per specificare la finestra proprietaria per qualsiasi finestra di dialogo o finestra di messaggio che può essere visualizzata dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="be37f-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="be37f-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="be37f-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="be37f-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="be37f-112">Type: **LPSTR**</span></span>

<span data-ttu-id="be37f-113">Indirizzo di una stringa con terminazione null che contiene il nome della directory iniziale.</span><span class="sxs-lookup"><span data-stu-id="be37f-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be37f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be37f-114">Return value</span></span>

<span data-ttu-id="be37f-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="be37f-115">Type: **DWORD**</span></span>

<span data-ttu-id="be37f-116">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="be37f-116">Returns one of the following values.</span></span>



| <span data-ttu-id="be37f-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="be37f-117">Return code</span></span>                                                                             | <span data-ttu-id="be37f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be37f-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="be37f-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="be37f-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="be37f-120">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="be37f-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="be37f-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="be37f-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="be37f-122">Un file non è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="be37f-122">A file was undeleted.</span></span> <span data-ttu-id="be37f-123">Gestione file ridisegna la finestra.</span><span class="sxs-lookup"><span data-stu-id="be37f-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="be37f-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="be37f-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="be37f-125">Nessun file eliminato.</span><span class="sxs-lookup"><span data-stu-id="be37f-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="be37f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be37f-126">Requirements</span></span>



| <span data-ttu-id="be37f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="be37f-127">Requirement</span></span> | <span data-ttu-id="be37f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="be37f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be37f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be37f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="be37f-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be37f-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be37f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be37f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="be37f-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be37f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be37f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be37f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="be37f-134"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="be37f-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




