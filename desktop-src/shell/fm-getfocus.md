---
description: Inviato da un'estensione di File Manager per recuperare il tipo di finestra di Gestione file con lo stato attivo per l'input.
title: FM_GETFOCUS messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841412"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="bbe0d-103">Messaggio \_ FM GETFOCUS</span><span class="sxs-lookup"><span data-stu-id="bbe0d-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="bbe0d-104">Inviato da un'estensione di File Manager per recuperare il tipo di finestra di Gestione file con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbe0d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe0d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe0d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbe0d-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bbe0d-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bbe0d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbe0d-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bbe0d-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe0d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe0d-110">Return value</span></span>

<span data-ttu-id="bbe0d-111">Restituisce il tipo di finestra di Gestione file con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="bbe0d-112">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-112">It can be one of the following values.</span></span>



| <span data-ttu-id="bbe0d-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bbe0d-113">Return code</span></span>                                                                                    | <span data-ttu-id="bbe0d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe0d-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="bbe0d-115"><dt>**FMFOCUS \_ DIR**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe0d-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="bbe0d-116">Parte della directory di una finestra della directory.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="bbe0d-117"><dt>**ALBERO \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe0d-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="bbe0d-118">Parte dell'albero di una finestra della directory.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="bbe0d-119"><dt>**UNITÀ \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe0d-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="bbe0d-120">Barra delle unità di una finestra della directory.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="bbe0d-121"><dt>**RICERCA \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe0d-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="bbe0d-122">Finestra Risultati ricerca.</span><span class="sxs-lookup"><span data-stu-id="bbe0d-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="bbe0d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe0d-123">Requirements</span></span>



| <span data-ttu-id="bbe0d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe0d-124">Requirement</span></span> | <span data-ttu-id="bbe0d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe0d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe0d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe0d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe0d-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbe0d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bbe0d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe0d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe0d-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbe0d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bbe0d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe0d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe0d-131"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe0d-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




