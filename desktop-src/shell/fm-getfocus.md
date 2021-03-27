---
description: Inviato da un'estensione di file Manager per recuperare il tipo di finestra di file Manager con lo stato attivo per l'input.
title: Messaggio FM_GETFOCUS (Wfext. h)
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
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979735"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="64a08-103">\_Messaggio FM GETfocus</span><span class="sxs-lookup"><span data-stu-id="64a08-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="64a08-104">Inviato da un'estensione di file Manager per recuperare il tipo di finestra di file Manager con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="64a08-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="64a08-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="64a08-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a08-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64a08-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="64a08-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="64a08-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="64a08-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64a08-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="64a08-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="64a08-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a08-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64a08-110">Return value</span></span>

<span data-ttu-id="64a08-111">Restituisce il tipo di finestra di file Manager con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="64a08-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="64a08-112">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="64a08-112">It can be one of the following values.</span></span>



| <span data-ttu-id="64a08-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="64a08-113">Return code</span></span>                                                                                    | <span data-ttu-id="64a08-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64a08-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="64a08-115"><dt>**\_dir FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="64a08-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="64a08-116">Parte della directory di una finestra di directory.</span><span class="sxs-lookup"><span data-stu-id="64a08-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="64a08-117"><dt>**\_albero FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="64a08-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="64a08-118">Parte albero di una finestra di directory.</span><span class="sxs-lookup"><span data-stu-id="64a08-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="64a08-119"><dt>**\_unità FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="64a08-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="64a08-120">Barra di unità di una finestra di directory.</span><span class="sxs-lookup"><span data-stu-id="64a08-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="64a08-121"><dt>**\_ricerca FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="64a08-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="64a08-122">Finestra Risultati ricerca.</span><span class="sxs-lookup"><span data-stu-id="64a08-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="64a08-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64a08-123">Requirements</span></span>



| <span data-ttu-id="64a08-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64a08-124">Requirement</span></span> | <span data-ttu-id="64a08-125">Valore</span><span class="sxs-lookup"><span data-stu-id="64a08-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64a08-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64a08-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64a08-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64a08-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="64a08-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64a08-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64a08-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64a08-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64a08-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64a08-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64a08-131"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a08-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




