---
description: AdminProperties deve essere creato nella tabella delle proprietà.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Proprietà AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333579"
---
# <a name="adminproperties-property"></a><span data-ttu-id="fdfb1-103">Proprietà AdminProperties</span><span class="sxs-lookup"><span data-stu-id="fdfb1-103">AdminProperties property</span></span>

<span data-ttu-id="fdfb1-104">**AdminProperties** deve essere creato nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="fdfb1-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="fdfb1-105">Il valore di **AdminProperties** è un elenco di nomi di proprietà separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="fdfb1-106">Il programma di installazione salva i valori di queste proprietà elencate al momento dell' [installazione amministrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="fdfb1-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="fdfb1-107">Quando gli utenti installano dall'immagine amministrativa, l'installazione usa i valori salvati delle proprietà, anziché i valori nel file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdfb1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdfb1-108">Remarks</span></span>

<span data-ttu-id="fdfb1-109">I nomi delle proprietà nell'elenco possono essere lettere maiuscole e minuscole (proprietà private) o tutte maiuscole (proprietà pubbliche).</span><span class="sxs-lookup"><span data-stu-id="fdfb1-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="fdfb1-110">Questa proprietà non deve terminare con un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdfb1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdfb1-111">Requirements</span></span>



| <span data-ttu-id="fdfb1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdfb1-112">Requirement</span></span> | <span data-ttu-id="fdfb1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="fdfb1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfb1-114">Versione</span><span class="sxs-lookup"><span data-stu-id="fdfb1-114">Version</span></span><br/> | <span data-ttu-id="fdfb1-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fdfb1-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fdfb1-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fdfb1-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fdfb1-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fdfb1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdfb1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdfb1-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fdfb1-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




