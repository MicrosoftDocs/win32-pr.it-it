---
description: Si tratta di un criterio di sistema per computer che può essere usato per applicare le regole dei componenti di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967683"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="e9091-103">EnforceUpgradeComponentRules</span><span class="sxs-lookup"><span data-stu-id="e9091-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="e9091-104">Si tratta di un criterio di [sistema](system-policy.md) per computer che può essere usato per applicare le regole dei componenti di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e9091-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="e9091-105">Impostare il criterio EnforceUpgradeComponentRules su 1 per applicare le regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md) di tutti i prodotti nel computer.</span><span class="sxs-lookup"><span data-stu-id="e9091-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="e9091-106">Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto, impostare la proprietà [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) su 1 nella riga di comando o nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9091-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="e9091-107">Quando la proprietà o il criterio è stato impostato su 1, [gli aggiornamenti piccoli](small-updates.md) e quelli [secondari](minor-upgrades.md) possono avere esito negativo perché l'aggiornamento tenta di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9091-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="e9091-108">Consente di aggiungere una nuova funzionalità alla parte superiore o centrale di un albero delle funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="e9091-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="e9091-109">La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="e9091-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="e9091-110">In questo caso, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e gli aggiornamenti possono essere considerati come un [aggiornamento importante](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e9091-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="e9091-111">Rimuovere un componente da una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e9091-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="e9091-112">Questa situazione può verificarsi anche se si modifica il GUID di un componente.</span><span class="sxs-lookup"><span data-stu-id="e9091-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="e9091-113">Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.</span><span class="sxs-lookup"><span data-stu-id="e9091-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="e9091-114">**Windows Installer 4,5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4,5 o versione successiva impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md) o impostando la proprietà [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="e9091-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="e9091-115">In alternativa, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e gli aggiornamenti possono essere considerati come un [aggiornamento importante](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e9091-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="e9091-116">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e9091-116">Registry Key</span></span>

<span data-ttu-id="e9091-117">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="e9091-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e9091-118">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e9091-118">Data Type</span></span>

<span data-ttu-id="e9091-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9091-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9091-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9091-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9091-121">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="e9091-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



