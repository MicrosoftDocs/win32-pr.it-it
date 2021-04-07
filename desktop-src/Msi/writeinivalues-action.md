---
description: L'azione WriteIniValues scrive le informazioni sul file ini che l'applicazione deve scrivere nei relativi file ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Azione WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882693"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="8e32b-103">Azione WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="8e32b-103">WriteIniValues Action</span></span>

<span data-ttu-id="8e32b-104">L'azione WriteIniValues scrive le informazioni sul file ini che l'applicazione deve scrivere nei relativi file ini.</span><span class="sxs-lookup"><span data-stu-id="8e32b-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="8e32b-105">La scrittura di queste informazioni viene gestita dalla tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e32b-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="8e32b-106">Viene scritto un valore ini se il componente corrispondente è stato impostato per essere installato localmente o eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="8e32b-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8e32b-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="8e32b-107">Sequence Restrictions</span></span>

<span data-ttu-id="8e32b-108">L'azione InstallValidate deve precedere l'azione WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="8e32b-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="8e32b-109">Se è presente un' [azione RemoveIniValues](removeinivalues-action.md) nella sequenza, è necessario che venga eseguita prima dell'azione WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="8e32b-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8e32b-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="8e32b-110">ActionData Messages</span></span>



| <span data-ttu-id="8e32b-111">Campo</span><span class="sxs-lookup"><span data-stu-id="8e32b-111">Field</span></span> | <span data-ttu-id="8e32b-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="8e32b-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="8e32b-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8e32b-113">\[1\]</span></span> | <span data-ttu-id="8e32b-114">Identificatore del file ini.</span><span class="sxs-lookup"><span data-stu-id="8e32b-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="8e32b-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8e32b-115">\[2\]</span></span> | <span data-ttu-id="8e32b-116">chiave del file ini nella sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="8e32b-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="8e32b-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="8e32b-117">\[3\]</span></span> | <span data-ttu-id="8e32b-118">Elemento rimosso dal file ini.</span><span class="sxs-lookup"><span data-stu-id="8e32b-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="8e32b-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="8e32b-119">\[4\]</span></span> | <span data-ttu-id="8e32b-120">Valore rimosso dal file ini.</span><span class="sxs-lookup"><span data-stu-id="8e32b-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="8e32b-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e32b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e32b-122">Tabella IniFile</span><span class="sxs-lookup"><span data-stu-id="8e32b-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



