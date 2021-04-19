---
description: L'azione RegisterFonts registra i tipi di carattere installati con il sistema. Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della tabella dei tipi di carattere al percorso del file del tipo di carattere installato.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Azione RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311709"
---
# <a name="registerfonts-action"></a><span data-ttu-id="df154-104">Azione RegisterFonts</span><span class="sxs-lookup"><span data-stu-id="df154-104">RegisterFonts Action</span></span>

<span data-ttu-id="df154-105">L'azione RegisterFonts registra i tipi di carattere installati con il sistema.</span><span class="sxs-lookup"><span data-stu-id="df154-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="df154-106">Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della [tabella dei tipi di carattere](font-table.md) al percorso del file del tipo di carattere installato.</span><span class="sxs-lookup"><span data-stu-id="df154-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="df154-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="df154-107">Sequence Restrictions</span></span>

<span data-ttu-id="df154-108">Prima di chiamare l'azione RegisterFonts, è necessario chiamare l'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="df154-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="df154-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="df154-109">ActionData Messages</span></span>



| <span data-ttu-id="df154-110">Campo</span><span class="sxs-lookup"><span data-stu-id="df154-110">Field</span></span> | <span data-ttu-id="df154-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="df154-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="df154-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="df154-112">\[1\]</span></span> | <span data-ttu-id="df154-113">File del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="df154-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="df154-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="df154-114">Remarks</span></span>

<span data-ttu-id="df154-115">L'azione RegisterFonts viene eseguita se il file specificato nella colonna file \_ della tabella dei [tipi di carattere](font-table.md) appartiene a un componente in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="df154-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



