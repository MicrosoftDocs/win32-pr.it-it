---
description: Impostare la proprietà MSIENFORCEUPGRADECOMPONENTRULES su 1 nella riga di comando o nella tabella delle proprietà per applicare le regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Proprietà MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329123"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="48aa9-103">Proprietà MSIENFORCEUPGRADECOMPONENTRULES</span><span class="sxs-lookup"><span data-stu-id="48aa9-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="48aa9-104">Impostare la proprietà **MSIENFORCEUPGRADECOMPONENTRULES** su 1 nella riga di comando o nella [tabella delle proprietà](property-table.md) per applicare le regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md) di un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="48aa9-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="48aa9-105">Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di tutti i prodotti nel computer, impostare il criterio [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) su 1.</span><span class="sxs-lookup"><span data-stu-id="48aa9-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="48aa9-106">Quando la proprietà o il criterio è impostato su 1, [gli aggiornamenti piccoli](small-updates.md) e [secondari](minor-upgrades.md) possono avere esito negativo perché l'aggiornamento tenta di eseguire le operazioni seguenti che violano le regole del componente di aggiornamento:</span><span class="sxs-lookup"><span data-stu-id="48aa9-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="48aa9-107">Consente di aggiungere una nuova funzionalità alla parte superiore o centrale di un albero delle funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="48aa9-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="48aa9-108">La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="48aa9-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="48aa9-109">In questo caso, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e l'aggiornamento può essere considerato un [aggiornamento importante](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="48aa9-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="48aa9-110">Rimuovere un componente da una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="48aa9-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="48aa9-111">Questa situazione può verificarsi anche se si modifica il GUID di un componente.</span><span class="sxs-lookup"><span data-stu-id="48aa9-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="48aa9-112">Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.</span><span class="sxs-lookup"><span data-stu-id="48aa9-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="48aa9-113">**Windows Installer 4,5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4,5 e versioni successive impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md) o impostando la proprietà [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="48aa9-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="48aa9-114">In alternativa, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e l'aggiornamento può essere considerato un [aggiornamento importante](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="48aa9-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48aa9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48aa9-115">Requirements</span></span>



| <span data-ttu-id="48aa9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="48aa9-116">Requirement</span></span> | <span data-ttu-id="48aa9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="48aa9-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48aa9-118">Versione</span><span class="sxs-lookup"><span data-stu-id="48aa9-118">Version</span></span><br/> | <span data-ttu-id="48aa9-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48aa9-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="48aa9-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48aa9-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="48aa9-121">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="48aa9-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="48aa9-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48aa9-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48aa9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48aa9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48aa9-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48aa9-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="48aa9-125">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="48aa9-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




