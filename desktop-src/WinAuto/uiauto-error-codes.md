---
title: Codici di errore (UIAutomationCoreApi. h)
description: Questo argomento descrive i codici di errore esposti dall'automazione interfaccia utente Microsoft.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047788"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="b2b83-103">Codici di errore (UIAutomationCoreApi. h)</span><span class="sxs-lookup"><span data-stu-id="b2b83-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="b2b83-104">Questo argomento descrive i codici di errore esposti dall'automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2b83-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="b2b83-105">L'elenco è ordinato in ordine alfabetico in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b2b83-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="b2b83-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b2b83-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="b2b83-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2b83-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="b2b83-108"><dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="b2b83-109">Indica che un metodo è stato chiamato su un elemento virtualizzato o su un elemento che non esiste più, in genere perché è stato eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="b2b83-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="b2b83-110"><dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="b2b83-111">Indica che è stato chiamato un metodo che richiede un elemento Enabled, ad esempio [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) o [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), su un elemento che è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b2b83-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="b2b83-112"><dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="b2b83-113">Indica che il metodo ha tentato di eseguire un'operazione non valida.</span><span class="sxs-lookup"><span data-stu-id="b2b83-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="b2b83-114"><dt>**UIA \_ E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="b2b83-115">Indica che il metodo [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) è stato chiamato su un elemento che non ha un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="b2b83-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="b2b83-116"><dt>**UIA \_ E \_ NotSupported**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="b2b83-117">Indica che il provider non supporta in modo esplicito la proprietà o il pattern di controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="b2b83-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="b2b83-118">Automazione interfaccia utente restituirà il codice di errore al chiamante senza tentare di fornire un valore predefinito o di eseguire il fallback a un altro provider.</span><span class="sxs-lookup"><span data-stu-id="b2b83-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="b2b83-119"><dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="b2b83-120">Indica che si è verificato un problema durante il caricamento di un assembly che contiene un provider del lato client (proxy).</span><span class="sxs-lookup"><span data-stu-id="b2b83-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="b2b83-121"><dt>**UIA \_ E \_ timeout**</dt> <dt>0x80131505</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="b2b83-122">Indica che il tempo assegnato per un processo o un'operazione è scaduto.</span><span class="sxs-lookup"><span data-stu-id="b2b83-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="b2b83-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2b83-123">Requirements</span></span>



| <span data-ttu-id="b2b83-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b83-124">Requirement</span></span> | <span data-ttu-id="b2b83-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b83-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b83-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b83-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2b83-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2b83-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b83-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2b83-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2b83-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2b83-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2b83-131"><dt>UIAutomationCoreApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b83-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





