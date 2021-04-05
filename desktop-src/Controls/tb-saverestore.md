---
title: Messaggio TB_SAVERESTORE (COMmctrl. h)
description: Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Controlli di Windows Message TB_SAVERESTORE
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873286"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="1c90a-104">TB \_ SAVERESTORE messaggio</span><span class="sxs-lookup"><span data-stu-id="1c90a-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="1c90a-105">Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1c90a-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c90a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c90a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c90a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c90a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c90a-108">Flag Save o Restore.</span><span class="sxs-lookup"><span data-stu-id="1c90a-108">Save or restore flag.</span></span> <span data-ttu-id="1c90a-109">Se questo parametro è **true**, le informazioni vengono salvate.</span><span class="sxs-lookup"><span data-stu-id="1c90a-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="1c90a-110">Se è **false**, le informazioni vengono ripristinate.</span><span class="sxs-lookup"><span data-stu-id="1c90a-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="1c90a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c90a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c90a-112">Puntatore a una struttura [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) che specifica la chiave del registro di sistema, la sottochiave e il nome del valore per le informazioni sullo stato della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1c90a-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c90a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c90a-113">Return value</span></span>

<span data-ttu-id="1c90a-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1c90a-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c90a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c90a-115">Remarks</span></span>

<span data-ttu-id="1c90a-116">Per la versione 4,72 e versioni precedenti, per usare questo messaggio per salvare o ripristinare una barra degli strumenti, la finestra padre del controllo Toolbar deve implementare un gestore per il codice di notifica [ \_ GETBUTTONINFO di TBN](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1c90a-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="1c90a-117">La barra degli strumenti Invia la notifica per recuperare le informazioni su ogni pulsante mentre viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="1c90a-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="1c90a-118">La versione 5,80 include una nuova opzione Salva/Ripristina.</span><span class="sxs-lookup"><span data-stu-id="1c90a-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="1c90a-119">All'inizio del processo, quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà una notifica [TBN \_ Save](tbn-save.md) o [TBN \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="1c90a-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="1c90a-120">Per utilizzare questa opzione, è necessario implementare i gestori delle notifiche per fornire la shell con le informazioni sulla bitmap e sullo stato necessarie per salvare o ripristinare lo stato della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1c90a-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c90a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c90a-121">Requirements</span></span>



| <span data-ttu-id="1c90a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c90a-122">Requirement</span></span> | <span data-ttu-id="1c90a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1c90a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c90a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c90a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1c90a-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c90a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c90a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c90a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1c90a-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c90a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c90a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c90a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c90a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c90a-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1c90a-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1c90a-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1c90a-131">**TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1c90a-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





