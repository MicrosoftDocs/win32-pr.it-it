---
description: L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla proprietà TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Azione InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967248"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="80d9a-103">Azione InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="80d9a-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="80d9a-104">L'azione InstallAdminPackage copia il database del prodotto nel punto di installazione amministrativa, definito dalla proprietà [**targetdir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="80d9a-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="80d9a-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="80d9a-105">Sequence Restrictions</span></span>

<span data-ttu-id="80d9a-106">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="80d9a-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="80d9a-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="80d9a-107">ActionData Messages</span></span>



| <span data-ttu-id="80d9a-108">Campo</span><span class="sxs-lookup"><span data-stu-id="80d9a-108">Field</span></span> | <span data-ttu-id="80d9a-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="80d9a-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="80d9a-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="80d9a-110">\[1\]</span></span> | <span data-ttu-id="80d9a-111">Nome dei file di installazione.</span><span class="sxs-lookup"><span data-stu-id="80d9a-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="80d9a-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="80d9a-112">\[6\]</span></span> | <span data-ttu-id="80d9a-113">Dimensioni del database.</span><span class="sxs-lookup"><span data-stu-id="80d9a-113">Size of database.</span></span>                                          |
| <span data-ttu-id="80d9a-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="80d9a-114">\[9\]</span></span> | <span data-ttu-id="80d9a-115">Identificatore dell'installazione amministrativa: directory del punto.</span><span class="sxs-lookup"><span data-stu-id="80d9a-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80d9a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="80d9a-116">Remarks</span></span>

<span data-ttu-id="80d9a-117">L'azione InstallAdminPackage aggiorna inoltre le informazioni di riepilogo del database e rimuove tutti i file CAB presenti nei flussi dopo la copia del database.</span><span class="sxs-lookup"><span data-stu-id="80d9a-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



