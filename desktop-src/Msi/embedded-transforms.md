---
description: Le trasformazioni incorporate vengono archiviate all'interno del file con estensione msi del pacchetto. Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile. In alternativa, le trasformazioni possono essere fornite agli utenti come file con estensione MST autonomo.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Trasformazioni incorporate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050146"
---
# <a name="embedded-transforms"></a><span data-ttu-id="3e6c4-105">Trasformazioni incorporate</span><span class="sxs-lookup"><span data-stu-id="3e6c4-105">Embedded Transforms</span></span>

<span data-ttu-id="3e6c4-106">Le trasformazioni incorporate vengono archiviate all'interno del file con estensione msi del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3e6c4-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="3e6c4-107">Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3e6c4-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="3e6c4-108">In alternativa, le trasformazioni possono essere fornite agli utenti come file con estensione MST autonomo.</span><span class="sxs-lookup"><span data-stu-id="3e6c4-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="3e6c4-109">Per aggiungere una trasformazione incorporata all'elenco di trasformazioni, aggiungere i due punti (:) prefisso per il nome file.</span><span class="sxs-lookup"><span data-stu-id="3e6c4-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="3e6c4-110">Poiché il programma di installazione può sempre ottenere la trasformazione dallo spazio di archiviazione nel file con estensione msi, le trasformazioni incorporate non vengono memorizzate nella cache nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e6c4-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="3e6c4-111">Le trasformazioni incorporate possono essere utilizzate in combinazione con trasformazioni [protette](secured-transforms.md) o [trasformazioni non protette](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c4-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="3e6c4-112">Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c4-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



