---
title: Messaggio CQPM_HELP (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per consentire all'estensione di pagina di visualizzare la Guida sensibile al contesto per la pagina.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119171"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="f673e-104">\_Messaggio della Guida CQPM</span><span class="sxs-lookup"><span data-stu-id="f673e-104">CQPM\_HELP message</span></span>

<span data-ttu-id="f673e-105">Il messaggio della **\_ Guida CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per consentire all'estensione di pagina di visualizzare la Guida sensibile al contesto per la pagina.</span><span class="sxs-lookup"><span data-stu-id="f673e-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="f673e-106">Se possibile, l'estensione della pagina query dovrebbe visualizzare la Guida sensibile al contesto in risposta a questo evento.</span><span class="sxs-lookup"><span data-stu-id="f673e-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="f673e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f673e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f673e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f673e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f673e-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f673e-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f673e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f673e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f673e-111">Puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) contenente dati aggiuntivi relativi alla voce di menu, al controllo, alla finestra di dialogo o alla finestra per la quale è richiesta la Guida sensibile al contesto.</span><span class="sxs-lookup"><span data-stu-id="f673e-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f673e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f673e-112">Return value</span></span>

<span data-ttu-id="f673e-113">Il valore restituito per questo messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f673e-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f673e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f673e-114">Requirements</span></span>



| <span data-ttu-id="f673e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f673e-115">Requirement</span></span> | <span data-ttu-id="f673e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f673e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f673e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f673e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f673e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f673e-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f673e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f673e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f673e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f673e-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f673e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f673e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f673e-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="f673e-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f673e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f673e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f673e-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="f673e-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="f673e-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="f673e-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

