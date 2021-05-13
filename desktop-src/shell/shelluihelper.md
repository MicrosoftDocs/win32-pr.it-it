---
description: Implementato da Shell per consentire agli sviluppatori di script e microsoft Visual Basic di usare alcune delle funzionalità disponibili in Shell. L'oggetto ShellUIHelper non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.
title: Oggetto ShellUIHelper (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842432"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="070df-105">Oggetto ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="070df-105">ShellUIHelper object</span></span>

<span data-ttu-id="070df-106">Implementato da Shell per consentire agli sviluppatori di script e microsoft Visual Basic di usare alcune delle funzionalità disponibili in Shell.</span><span class="sxs-lookup"><span data-stu-id="070df-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="070df-107">**L'oggetto ShellUIHelper** non ha proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="070df-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="070df-108">Vengono forniti metodi per aggiungere elementi alla shell.</span><span class="sxs-lookup"><span data-stu-id="070df-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="070df-109">Membri</span><span class="sxs-lookup"><span data-stu-id="070df-109">Members</span></span>

<span data-ttu-id="070df-110">**L'oggetto ShellUIHelper** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="070df-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="070df-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="070df-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="070df-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="070df-112">Methods</span></span>

<span data-ttu-id="070df-113">**L'oggetto ShellUIHelper** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="070df-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="070df-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="070df-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="070df-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="070df-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="070df-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="070df-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="070df-117">Aggiunge un nuovo canale all'elenco di canali nel <strong>menu</strong> Preferiti Internet Explorer canale e alla barra <strong>Dei</strong> canali sul desktop.</span><span class="sxs-lookup"><span data-stu-id="070df-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="070df-118">Questo metodo non è più supportato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="070df-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="070df-119">In tale sistema operativo, restituisce E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="070df-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="070df-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="070df-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="070df-121">Aggiunge un elemento al Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="070df-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="070df-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="070df-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="070df-123">Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="070df-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="070df-124">L'interfaccia utente viene inizializzata sui parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="070df-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="070df-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="070df-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="070df-126">Indica se un URL specificato è sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="070df-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="070df-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="070df-127">Requirements</span></span>



| <span data-ttu-id="070df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="070df-128">Requirement</span></span> | <span data-ttu-id="070df-129">Valore</span><span class="sxs-lookup"><span data-stu-id="070df-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070df-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="070df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="070df-131">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="070df-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="070df-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="070df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="070df-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="070df-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="070df-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="070df-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="070df-135"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="070df-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="070df-136">DLL</span><span class="sxs-lookup"><span data-stu-id="070df-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="070df-137"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="070df-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




