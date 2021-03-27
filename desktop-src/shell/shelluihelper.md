---
description: Implementato dalla Shell per consentire agli sviluppatori di script e Microsoft Visual Basic di usare alcune delle funzionalità disponibili nella shell. L'oggetto ShellUIHelper non dispone di proprietà o eventi. Sono disponibili metodi per aggiungere elementi alla Shell.
title: Oggetto ShellUIHelper (Exdisp. h)
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
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980719"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="2ba51-105">Oggetto ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="2ba51-105">ShellUIHelper object</span></span>

<span data-ttu-id="2ba51-106">Implementato dalla Shell per consentire agli sviluppatori di script e Microsoft Visual Basic di usare alcune delle funzionalità disponibili nella shell.</span><span class="sxs-lookup"><span data-stu-id="2ba51-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="2ba51-107">L'oggetto **ShellUIHelper** non dispone di proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="2ba51-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="2ba51-108">Sono disponibili metodi per aggiungere elementi alla Shell.</span><span class="sxs-lookup"><span data-stu-id="2ba51-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="2ba51-109">Membri</span><span class="sxs-lookup"><span data-stu-id="2ba51-109">Members</span></span>

<span data-ttu-id="2ba51-110">L'oggetto **ShellUIHelper** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2ba51-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="2ba51-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ba51-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ba51-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2ba51-112">Methods</span></span>

<span data-ttu-id="2ba51-113">L'oggetto **ShellUIHelper** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2ba51-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2ba51-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2ba51-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2ba51-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ba51-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2ba51-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ba51-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2ba51-117">Consente di aggiungere un nuovo canale all'elenco di canali nel menu <strong>Preferiti</strong> di Internet Explorer e alla barra del <strong>canale</strong> sul desktop.</span><span class="sxs-lookup"><span data-stu-id="2ba51-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2ba51-118">Questo metodo non è più supportato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ba51-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="2ba51-119">In tale sistema operativo restituisce E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2ba51-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2ba51-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ba51-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2ba51-121">Aggiunge un elemento al desktop attivo.</span><span class="sxs-lookup"><span data-stu-id="2ba51-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2ba51-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ba51-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2ba51-123">Visualizza l'interfaccia utente predefinita per la creazione di un elemento preferito.</span><span class="sxs-lookup"><span data-stu-id="2ba51-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="2ba51-124">L'interfaccia utente viene inizializzata sui parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="2ba51-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2ba51-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ba51-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="2ba51-126">Indica se un URL specificato è sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="2ba51-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2ba51-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ba51-127">Requirements</span></span>



| <span data-ttu-id="2ba51-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ba51-128">Requirement</span></span> | <span data-ttu-id="2ba51-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2ba51-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba51-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ba51-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba51-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ba51-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2ba51-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ba51-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba51-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ba51-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2ba51-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ba51-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ba51-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ba51-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="2ba51-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2ba51-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ba51-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2ba51-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




