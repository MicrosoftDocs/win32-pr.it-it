---
description: L'azione SetODBCFolders controlla i driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Azione SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305962"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="a7db9-103">Azione SetODBCFolders</span><span class="sxs-lookup"><span data-stu-id="a7db9-103">SetODBCFolders Action</span></span>

<span data-ttu-id="a7db9-104">L'azione SetODBCFolders controlla i driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.</span><span class="sxs-lookup"><span data-stu-id="a7db9-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a7db9-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="a7db9-105">Sequence Restrictions</span></span>

<span data-ttu-id="a7db9-106">L'azione SetODBCFolders deve essere successiva all'azione [CostFinalize secondo](costfinalize-action.md) e prima dell' [azione InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="a7db9-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a7db9-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="a7db9-107">ActionData Messages</span></span>



| <span data-ttu-id="a7db9-108">Campo</span><span class="sxs-lookup"><span data-stu-id="a7db9-108">Field</span></span> | <span data-ttu-id="a7db9-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="a7db9-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7db9-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a7db9-110">\[1\]</span></span> | <span data-ttu-id="a7db9-111">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="a7db9-111">Driver description.</span></span> <span data-ttu-id="a7db9-112">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="a7db9-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="a7db9-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a7db9-113">\[2\]</span></span> | <span data-ttu-id="a7db9-114">Percorso della cartella originale del nuovo driver.</span><span class="sxs-lookup"><span data-stu-id="a7db9-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="a7db9-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a7db9-115">\[3\]</span></span> | <span data-ttu-id="a7db9-116">Nuovo percorso della cartella per il nuovo driver.</span><span class="sxs-lookup"><span data-stu-id="a7db9-116">New folder location for the new driver.</span></span> <span data-ttu-id="a7db9-117">Si tratta del percorso di un driver esistente.</span><span class="sxs-lookup"><span data-stu-id="a7db9-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a7db9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7db9-118">Remarks</span></span>

<span data-ttu-id="a7db9-119">Questa azione inserisce un nuovo driver nella stessa directory del driver esistente da sostituire.</span><span class="sxs-lookup"><span data-stu-id="a7db9-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="a7db9-120">L'azione SetODBCFolders utilizza la [tabella directory](directory-table.md) per impostare i percorsi dei driver esistenti che devono essere sostituiti.</span><span class="sxs-lookup"><span data-stu-id="a7db9-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



