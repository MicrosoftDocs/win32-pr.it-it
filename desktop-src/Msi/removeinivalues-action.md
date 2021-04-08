---
description: L'azione RemoveIniValues rimuove le informazioni sul file ini specificate per la rimozione nella tabella RemoveIniFile se il componente è impostato per essere installato localmente o da Run-from-source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Azione RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968509"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="9bafb-103">Azione RemoveIniValues</span><span class="sxs-lookup"><span data-stu-id="9bafb-103">RemoveIniValues Action</span></span>

<span data-ttu-id="9bafb-104">L'azione RemoveIniValues rimuove le informazioni sul file ini specificate per la rimozione nella [tabella RemoveIniFile](removeinifile-table.md) se il componente è impostato per essere installato localmente o da Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="9bafb-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="9bafb-105">L'azione RemoveIniValues rimuove le informazioni sul file ini associate a un componente nella [tabella inifile](inifile-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bafb-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="9bafb-106">Questa azione rimuove anche le informazioni sul file ini se le informazioni sono state scritte dall' [azione WriteIniValues](writeinivalues-action.md) e il componente è pianificato per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="9bafb-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9bafb-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="9bafb-107">Sequence Restrictions</span></span>

<span data-ttu-id="9bafb-108">L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima dell'azione RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="9bafb-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="9bafb-109">Se nella sequenza viene utilizzata un'azione [WriteIniValues](writeinivalues-action.md) , è necessario che venga visualizzata dopo RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="9bafb-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9bafb-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="9bafb-110">ActionData Messages</span></span>



| <span data-ttu-id="9bafb-111">Campo</span><span class="sxs-lookup"><span data-stu-id="9bafb-111">Field</span></span> | <span data-ttu-id="9bafb-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="9bafb-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="9bafb-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9bafb-113">\[1\]</span></span> | <span data-ttu-id="9bafb-114">Identificatore del file ini.</span><span class="sxs-lookup"><span data-stu-id="9bafb-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="9bafb-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="9bafb-115">\[2\]</span></span> | <span data-ttu-id="9bafb-116">Sezione chiave del file ini.</span><span class="sxs-lookup"><span data-stu-id="9bafb-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="9bafb-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="9bafb-117">\[3\]</span></span> | <span data-ttu-id="9bafb-118">Elemento rimosso dal file ini.</span><span class="sxs-lookup"><span data-stu-id="9bafb-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="9bafb-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="9bafb-119">\[4\]</span></span> | <span data-ttu-id="9bafb-120">Valore rimosso dal file ini.</span><span class="sxs-lookup"><span data-stu-id="9bafb-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bafb-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bafb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bafb-122">Tabella RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="9bafb-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="9bafb-123">Tabella IniFile</span><span class="sxs-lookup"><span data-stu-id="9bafb-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="9bafb-124">Azione WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="9bafb-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="9bafb-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="9bafb-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



