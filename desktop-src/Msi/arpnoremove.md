---
description: L'impostazione della proprietà ARPNOREMOVE Disabilita la funzionalità Installazione applicazioni nel pannello di controllo che consente di rimuovere il prodotto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Proprietà ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328020"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="c6c35-103">Proprietà ARPNOREMOVE</span><span class="sxs-lookup"><span data-stu-id="c6c35-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="c6c35-104">L'impostazione della proprietà **ARPNOREMOVE** Disabilita la funzionalità **Installazione applicazioni** nel **Pannello di controllo** che consente di rimuovere il prodotto.</span><span class="sxs-lookup"><span data-stu-id="c6c35-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="c6c35-105">Per Windows 2000, Disabilita il pulsante **Rimuovi** per il prodotto da **Installazione applicazioni** nel **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="c6c35-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="c6c35-106">Per i sistemi operativi precedenti, ciò comporta la rimozione del prodotto dall'elenco dei prodotti installati in installazione **applicazioni** nel **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="c6c35-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="c6c35-107">Se la proprietà **ARPNOREMOVE** è impostata, l' [azione RegisterProduct](registerproduct-action.md) scrive il valore "NoRemove" nella chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="c6c35-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="c6c35-108">**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **{*codice Product Key*}**</span><span class="sxs-lookup"><span data-stu-id="c6c35-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="c6c35-109">L'impostazione della proprietà **ARPNOREMOVE** impedisce la scrittura del valore UninstallString sotto questa chiave.</span><span class="sxs-lookup"><span data-stu-id="c6c35-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="c6c35-110">Il valore UnistallString è una riga di comando per la rimozione del prodotto, invece della riconfigurazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c6c35-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c35-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6c35-111">Remarks</span></span>

<span data-ttu-id="c6c35-112">Questa proprietà può essere impostata, ad esempio, durante una trasformazione di personalizzazione per impedire agli utenti di rimuovere una personalizzazione di amministratore.</span><span class="sxs-lookup"><span data-stu-id="c6c35-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c35-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6c35-113">Requirements</span></span>



| <span data-ttu-id="c6c35-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c35-114">Requirement</span></span> | <span data-ttu-id="c6c35-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c6c35-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c35-116">Versione</span><span class="sxs-lookup"><span data-stu-id="c6c35-116">Version</span></span><br/> | <span data-ttu-id="c6c35-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6c35-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c6c35-118">Windows Installer 4,0 o Windows Installer 4,5 o versione successiva in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6c35-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="c6c35-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6c35-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c6c35-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c6c35-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6c35-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6c35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c35-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6c35-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




