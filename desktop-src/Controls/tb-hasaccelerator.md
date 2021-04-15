---
title: Messaggio TB_HASACCELERATOR (COMmctrl. h)
description: Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di accelerazione specificato.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Controlli di Windows Message TB_HASACCELERATOR
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477104"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="d8063-104">TB \_ HASACCELERATOR messaggio</span><span class="sxs-lookup"><span data-stu-id="d8063-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="d8063-105">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d8063-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="d8063-106">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8063-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="d8063-107">Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di accelerazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d8063-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8063-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8063-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8063-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8063-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8063-110">Oggetto **WCHAR** che rappresenta il carattere dell'acceleratore di input da testare.</span><span class="sxs-lookup"><span data-stu-id="d8063-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="d8063-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8063-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8063-112">Puntatore a un valore **int** che riceve il numero di pulsanti con il carattere di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="d8063-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8063-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8063-113">Return value</span></span>

<span data-ttu-id="d8063-114">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d8063-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="d8063-115">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="d8063-115">Security Considerations</span></span>

<span data-ttu-id="d8063-116">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="d8063-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8063-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8063-117">Remarks</span></span>

<span data-ttu-id="d8063-118">Innanzitutto, il sistema esegue una query su tutti i pulsanti della barra degli strumenti per individuare gli acceleratori corrispondenti</span><span class="sxs-lookup"><span data-stu-id="d8063-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="d8063-119">Se non viene trovata alcuna corrispondenza, il sistema invia la notifica [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) alla finestra padre, richiedendo l'indice del pulsante con il carattere di accelerazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d8063-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="d8063-120">Se l'elemento padre fornisce un indice, il conteggio viene impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="d8063-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8063-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8063-121">Requirements</span></span>



| <span data-ttu-id="d8063-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8063-122">Requirement</span></span> | <span data-ttu-id="d8063-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d8063-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8063-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8063-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d8063-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8063-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8063-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8063-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d8063-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8063-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8063-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8063-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8063-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8063-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





