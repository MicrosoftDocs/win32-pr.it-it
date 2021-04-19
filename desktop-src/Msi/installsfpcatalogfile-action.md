---
description: L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per la protezione dei file di Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Azione InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305965"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="0ea87-103">Azione InstallSFPCatalogFile</span><span class="sxs-lookup"><span data-stu-id="0ea87-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="0ea87-104">L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per la protezione dei file di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ea87-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="0ea87-105">InstallSFPCatalogFile esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella [FileSFPCatalog](filesfpcatalog-table.md) e sulla [tabella SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ea87-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="0ea87-106">I cataloghi vengono installati se sono associati a un file in un componente impostato per l'installazione locale o se sono associati a un file da ripristinare in un componente installato localmente.</span><span class="sxs-lookup"><span data-stu-id="0ea87-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0ea87-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="0ea87-107">Sequence Restrictions</span></span>

<span data-ttu-id="0ea87-108">L'azione InstallSFPCatalogFile deve essere sequenziata prima di [InstallFiles](installfiles-action.md) e dopo [CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0ea87-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0ea87-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="0ea87-109">ActionData Messages</span></span>



| <span data-ttu-id="0ea87-110">Campo</span><span class="sxs-lookup"><span data-stu-id="0ea87-110">Field</span></span> | <span data-ttu-id="0ea87-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="0ea87-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="0ea87-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0ea87-112">\[1\]</span></span> | <span data-ttu-id="0ea87-113">Nome del catalogo da installare.</span><span class="sxs-lookup"><span data-stu-id="0ea87-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="0ea87-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="0ea87-114">\[2\]</span></span> | <span data-ttu-id="0ea87-115">Nome del catalogo da cui dipende l'installazione di questo catalogo.</span><span class="sxs-lookup"><span data-stu-id="0ea87-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0ea87-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ea87-116">Remarks</span></span>

<span data-ttu-id="0ea87-117">Catalogo che dipende da un altro catalogo installato dopo il catalogo padre.</span><span class="sxs-lookup"><span data-stu-id="0ea87-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



