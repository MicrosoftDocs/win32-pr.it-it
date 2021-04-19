---
description: L'azione UnregisterFonts rimuove le informazioni di registrazione sui tipi di carattere installati dal sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Azione UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319418"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="d24ca-103">Azione UnregisterFonts</span><span class="sxs-lookup"><span data-stu-id="d24ca-103">UnregisterFonts Action</span></span>

<span data-ttu-id="d24ca-104">L'azione UnregisterFonts rimuove le informazioni di registrazione sui tipi di carattere installati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d24ca-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d24ca-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="d24ca-105">Sequence Restrictions</span></span>

<span data-ttu-id="d24ca-106">L'azione [RemoveFiles](removefiles-action.md) deve essere chiamata dopo UnregisterFonts.</span><span class="sxs-lookup"><span data-stu-id="d24ca-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d24ca-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="d24ca-107">ActionData Messages</span></span>



| <span data-ttu-id="d24ca-108">Campo</span><span class="sxs-lookup"><span data-stu-id="d24ca-108">Field</span></span> | <span data-ttu-id="d24ca-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="d24ca-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d24ca-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d24ca-110">\[1\]</span></span> | <span data-ttu-id="d24ca-111">File del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d24ca-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="d24ca-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d24ca-112">Remarks</span></span>

<span data-ttu-id="d24ca-113">L'azione UnregisterFonts viene eseguita se il file specificato nella colonna file \_ della tabella dei [tipi di carattere](font-table.md) appartiene a un componente di cui è in corso la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="d24ca-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



