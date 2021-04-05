---
description: Lo stato di installazione di un file complementare dipende non dalle informazioni relative al controllo delle versioni dei file, bensì al controllo delle versioni del padre complementare.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: File complementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968021"
---
# <a name="companion-files"></a><span data-ttu-id="56f32-103">File complementari</span><span class="sxs-lookup"><span data-stu-id="56f32-103">Companion Files</span></span>

<span data-ttu-id="56f32-104">Lo stato di installazione di un file complementare dipende non dalle informazioni relative al controllo delle versioni dei file, bensì al controllo delle versioni del padre complementare.</span><span class="sxs-lookup"><span data-stu-id="56f32-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="56f32-105">Vedere le [regole di controllo delle versioni dei file](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="56f32-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="56f32-106">Per specificare un file complementare, la chiave primaria dell'elemento padre complementare nella [tabella file](file-table.md) deve essere creata nella colonna Version del record per il complemento.</span><span class="sxs-lookup"><span data-stu-id="56f32-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="56f32-107">Nell'esempio seguente, Filea è l'elemento padre complementare e FileB è il file complementare.</span><span class="sxs-lookup"><span data-stu-id="56f32-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="56f32-108">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="56f32-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="56f32-109">File</span><span class="sxs-lookup"><span data-stu-id="56f32-109">File</span></span>  | <span data-ttu-id="56f32-110">Versione</span><span class="sxs-lookup"><span data-stu-id="56f32-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="56f32-111">FileA</span><span class="sxs-lookup"><span data-stu-id="56f32-111">FileA</span></span> | <span data-ttu-id="56f32-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="56f32-112">1.0.0.0</span></span> |
| <span data-ttu-id="56f32-113">FileB</span><span class="sxs-lookup"><span data-stu-id="56f32-113">FileB</span></span> | <span data-ttu-id="56f32-114">FileA</span><span class="sxs-lookup"><span data-stu-id="56f32-114">FileA</span></span>   |



 

<span data-ttu-id="56f32-115">In questo esempio, lo stato di installazione di FileB dipende dalle [regole di controllo delle versioni dei file](file-versioning-rules.md) e dalle informazioni sul controllo delle versioni per file a.</span><span class="sxs-lookup"><span data-stu-id="56f32-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="56f32-116">Se il programma di installazione stabilisce che la versione di Filea nel pacchetto deve essere installata su una versione precedente di Filea già esistente nel computer dell'utente, installerà anche FileB dal pacchetto indipendentemente dalla versione di qualsiasi FileB installato.</span><span class="sxs-lookup"><span data-stu-id="56f32-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="56f32-117">Si noti che un file che rappresenta il percorso della chiave per il componente non deve essere un file complementare.</span><span class="sxs-lookup"><span data-stu-id="56f32-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="56f32-118">Questo comporterebbe la logica di controllo delle versioni del file del percorso della chiave determinata dal file padre complementare.</span><span class="sxs-lookup"><span data-stu-id="56f32-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



