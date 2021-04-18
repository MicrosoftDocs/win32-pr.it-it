---
description: L'impostazione della proprietà ARPNOMODIFY Disabilita la funzionalità di installazione applicazioni nel pannello di controllo che modifica il prodotto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Proprietà ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328026"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="1dffc-103">Proprietà ARPNOMODIFY</span><span class="sxs-lookup"><span data-stu-id="1dffc-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="1dffc-104">L'impostazione della proprietà **ARPNOMODIFY** Disabilita la funzionalità di installazione applicazioni nel pannello di controllo che modifica il prodotto.</span><span class="sxs-lookup"><span data-stu-id="1dffc-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="1dffc-105">Per Windows 2000, Disabilita il pulsante **modifica** per il prodotto in **Installazione applicazioni** nel **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="1dffc-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="1dffc-106">Nei sistemi operativi precedenti, se si fa clic sul pulsante installazione **applicazioni** , il prodotto viene disinstallato, anziché in modalità di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="1dffc-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="1dffc-107">Se la proprietà **ARPNOMODIFY** è impostata, l' [azione RegisterProduct](registerproduct-action.md) scrive il valore "nomodify" nella chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1dffc-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="1dffc-108">**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **{*codice Product Key*}**</span><span class="sxs-lookup"><span data-stu-id="1dffc-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="1dffc-109">Se la proprietà **ARPNOMODIFY** è impostata e la proprietà [**ARPNOREMOVE**](arpnoremove.md) non è impostata, l'azione RegisterProduct scrive anche il valore UninstallString in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="1dffc-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="1dffc-110">Il valore UnistallString è una riga di comando per la rimozione del prodotto, invece della riconfigurazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1dffc-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dffc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dffc-111">Remarks</span></span>

<span data-ttu-id="1dffc-112">In Windows 2000, in questo modo il pulsante **Cambia** per il prodotto viene disabilitato in **Installazione applicazioni** del pannello di **controllo**.</span><span class="sxs-lookup"><span data-stu-id="1dffc-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="1dffc-113">Questa proprietà può essere impostata da una trasformazione di personalizzazione per impedire agli utenti di modificare la personalizzazione di un amministratore tramite **Installazione applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="1dffc-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="1dffc-114">Questa proprietà ha effetto solo su **Installazione applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="1dffc-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dffc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dffc-115">Requirements</span></span>



| <span data-ttu-id="1dffc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dffc-116">Requirement</span></span> | <span data-ttu-id="1dffc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1dffc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dffc-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1dffc-118">Version</span></span><br/> | <span data-ttu-id="1dffc-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1dffc-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1dffc-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dffc-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1dffc-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1dffc-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1dffc-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1dffc-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1dffc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dffc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dffc-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1dffc-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1dffc-125">Esempio di trasformazione della personalizzazione</span><span class="sxs-lookup"><span data-stu-id="1dffc-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




