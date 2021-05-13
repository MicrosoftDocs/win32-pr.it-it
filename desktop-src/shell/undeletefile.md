---
description: Specifica una funzione di callback definita dall'applicazione chiamata da File Manager quando l'utente sceglie il comando Annulla eliminazione dal menu File.
title: FM_UNDELETE_PROC puntatore a funzione (Wfext.h)
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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842422"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="0cd93-103">Puntatore alla funzione FM \_ UNDELETE \_ PROC</span><span class="sxs-lookup"><span data-stu-id="0cd93-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="0cd93-104">Specifica una funzione di callback definita dall'applicazione chiamata da  File Manager quando l'utente sceglie il comando Annulla eliminazione dal menu **File.**</span><span class="sxs-lookup"><span data-stu-id="0cd93-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd93-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cd93-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="0cd93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cd93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd93-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="0cd93-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="0cd93-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="0cd93-108">Type: **HWND**</span></span>

<span data-ttu-id="0cd93-109">Handle di finestra per File Manager.</span><span class="sxs-lookup"><span data-stu-id="0cd93-109">The window handle to File Manager.</span></span> <span data-ttu-id="0cd93-110">Una DLL di annullamento dell'eliminazione deve utilizzare questo handle per specificare la finestra del proprietario per qualsiasi finestra di dialogo o finestra di messaggio che potrebbe essere visualizzata nella DLL.</span><span class="sxs-lookup"><span data-stu-id="0cd93-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="0cd93-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="0cd93-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="0cd93-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="0cd93-112">Type: **LPSTR**</span></span>

<span data-ttu-id="0cd93-113">Indirizzo di una stringa con terminazione Null che contiene il nome della directory iniziale.</span><span class="sxs-lookup"><span data-stu-id="0cd93-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd93-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cd93-114">Return value</span></span>

<span data-ttu-id="0cd93-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cd93-115">Type: **DWORD**</span></span>

<span data-ttu-id="0cd93-116">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0cd93-116">Returns one of the following values.</span></span>



| <span data-ttu-id="0cd93-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0cd93-117">Return code</span></span>                                                                             | <span data-ttu-id="0cd93-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cd93-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cd93-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="0cd93-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="0cd93-120">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="0cd93-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0cd93-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cd93-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="0cd93-122">È stata annullata l'eliminazione di un file.</span><span class="sxs-lookup"><span data-stu-id="0cd93-122">A file was undeleted.</span></span> <span data-ttu-id="0cd93-123">File Manager ridisegna la finestra.</span><span class="sxs-lookup"><span data-stu-id="0cd93-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="0cd93-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="0cd93-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="0cd93-125">Nessun file è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="0cd93-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0cd93-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cd93-126">Requirements</span></span>



| <span data-ttu-id="0cd93-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd93-127">Requirement</span></span> | <span data-ttu-id="0cd93-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0cd93-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd93-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cd93-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd93-130">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0cd93-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cd93-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cd93-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd93-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cd93-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0cd93-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cd93-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cd93-134"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd93-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




