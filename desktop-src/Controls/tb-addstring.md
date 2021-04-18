---
title: Messaggio TB_ADDSTRING (COMmctrl. h)
description: Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Controlli di Windows Message TB_ADDSTRING
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302788"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="83e80-104">TB \_ ADDSTRING messaggio</span><span class="sxs-lookup"><span data-stu-id="83e80-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="83e80-105">Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="83e80-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="83e80-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83e80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e80-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83e80-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83e80-108">Handle per l'istanza del modulo con un file eseguibile che contiene la risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="83e80-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="83e80-109">Se *lParam* punta invece a una matrice di caratteri con una o più stringhe, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="83e80-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="83e80-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83e80-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83e80-111">Identificatore di risorsa per la risorsa di stringa o puntatore a una matrice TCHAR.</span><span class="sxs-lookup"><span data-stu-id="83e80-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="83e80-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="83e80-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83e80-113">Return value</span></span>

<span data-ttu-id="83e80-114">Restituisce l'indice della prima nuova stringa se ha esito positivo oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="83e80-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e80-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="83e80-115">Remarks</span></span>

<span data-ttu-id="83e80-116">Se *wParam* è **null**, *lParam* punta a una matrice di caratteri con una o più stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="83e80-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="83e80-117">L'ultima stringa della matrice deve terminare con due caratteri null.</span><span class="sxs-lookup"><span data-stu-id="83e80-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="83e80-118">Se *wParam* è il hInstance dell'applicazione o di un altro modulo contenente una risorsa di stringa, *lParam* è l'identificatore di risorsa della stringa.</span><span class="sxs-lookup"><span data-stu-id="83e80-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="83e80-119">Ogni elemento nella stringa deve iniziare con un carattere separatore arbitrario e la stringa deve terminare con due caratteri di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="83e80-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="83e80-120">Ad esempio, il testo per tre pulsanti potrebbe essere visualizzato nella tabella delle stringhe come "/New/Open/Save//".</span><span class="sxs-lookup"><span data-stu-id="83e80-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="83e80-121">Il messaggio restituisce l'indice di "New" nel pool di stringhe della barra degli strumenti e gli altri elementi si trovano in posizioni consecutive.</span><span class="sxs-lookup"><span data-stu-id="83e80-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e80-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e80-122">Requirements</span></span>



| <span data-ttu-id="83e80-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e80-123">Requirement</span></span> | <span data-ttu-id="83e80-124">Valore</span><span class="sxs-lookup"><span data-stu-id="83e80-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83e80-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e80-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83e80-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83e80-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83e80-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e80-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83e80-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83e80-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83e80-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e80-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e80-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e80-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="83e80-131">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="83e80-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83e80-132">**TB \_ ADDSTRINGW** (Unicode) e **TB \_ ADDSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="83e80-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





