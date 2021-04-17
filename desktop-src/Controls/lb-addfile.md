---
title: Messaggio LB_ADDFILE (winuser. h)
description: Aggiunge il nome file specificato a una casella di riepilogo contenente un elenco di directory.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- Controlli di Windows Message LB_ADDFILE
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478262"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="4241d-104">\_Messaggio AddFile lb</span><span class="sxs-lookup"><span data-stu-id="4241d-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="4241d-105">Aggiunge il nome file specificato a una casella di riepilogo contenente un elenco di directory.</span><span class="sxs-lookup"><span data-stu-id="4241d-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="4241d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4241d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4241d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4241d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4241d-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4241d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4241d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4241d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4241d-110">Puntatore a un buffer che specifica il nome del file da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4241d-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4241d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4241d-111">Return value</span></span>

<span data-ttu-id="4241d-112">Il valore restituito è l'indice in base zero del file che è stato aggiunto oppure LB \_ Err se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4241d-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="4241d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4241d-113">Remarks</span></span>

<span data-ttu-id="4241d-114">La casella di riepilogo a cui viene aggiunto *lParam* deve essere stata compilata dalla funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .</span><span class="sxs-lookup"><span data-stu-id="4241d-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="4241d-115">Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100).</span><span class="sxs-lookup"><span data-stu-id="4241d-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="4241d-116">Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ AddFile** il tempo più breve possibile.</span><span class="sxs-lookup"><span data-stu-id="4241d-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="4241d-117">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4241d-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="4241d-118">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.</span><span class="sxs-lookup"><span data-stu-id="4241d-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="4241d-119">Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="4241d-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="4241d-120">Ciò può causare problemi.</span><span class="sxs-lookup"><span data-stu-id="4241d-120">This can cause problems.</span></span> <span data-ttu-id="4241d-121">Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati.</span><span class="sxs-lookup"><span data-stu-id="4241d-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="4241d-122">Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="4241d-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4241d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4241d-123">Requirements</span></span>



| <span data-ttu-id="4241d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4241d-124">Requirement</span></span> | <span data-ttu-id="4241d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4241d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4241d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4241d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4241d-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4241d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4241d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4241d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4241d-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4241d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4241d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4241d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4241d-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4241d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4241d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4241d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="4241d-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4241d-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4241d-134">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="4241d-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="4241d-135">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="4241d-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





