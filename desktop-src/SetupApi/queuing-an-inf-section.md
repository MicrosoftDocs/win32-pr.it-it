---
description: Oltre ad accodare singolarmente le operazioni sui file, è anche possibile accodare tutti i file elencati in una sezione INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Accodamento di una sezione INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529778"
---
# <a name="queuing-an-inf-section"></a><span data-ttu-id="936a7-103">Accodamento di una sezione INF</span><span class="sxs-lookup"><span data-stu-id="936a7-103">Queuing an INF Section</span></span>

<span data-ttu-id="936a7-104">Oltre ad accodare singolarmente le operazioni sui file, è anche possibile accodare tutti i file elencati in una sezione INF.</span><span class="sxs-lookup"><span data-stu-id="936a7-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="936a7-105">È possibile accodare tutti i file elencati in una sezione **copia file** di un file inf chiamando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span><span class="sxs-lookup"><span data-stu-id="936a7-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="936a7-106">Affinché questa funzione abbia esito positivo, la sezione **copia file** deve essere nel formato corretto e il file inf, o uno dei file accodati, deve contenere le sezioni **SourceDisksFiles** e **SourceDisksNames** .</span><span class="sxs-lookup"><span data-stu-id="936a7-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="936a7-107">Analogamente, se si desidera eliminare tutti i file specificati in una sezione dei file di **eliminazione** di un file inf, è possibile chiamare [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span><span class="sxs-lookup"><span data-stu-id="936a7-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="936a7-108">Per rinominare tutti i file in una sezione **Rinomina file** di un file inf, usare [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="936a7-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



