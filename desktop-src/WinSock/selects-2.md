---
description: Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione Select era lo standard (e solo) indica di ottenere le indicazioni relative agli eventi di rete.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Seleziona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309936"
---
# <a name="selects"></a><span data-ttu-id="ab0ef-103">Seleziona</span><span class="sxs-lookup"><span data-stu-id="ab0ef-103">Selects</span></span>

<span data-ttu-id="ab0ef-104">Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era lo standard (e solo) indica di ottenere le indicazioni relative agli eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-104">In the original Berkeley Software Distribution (BSD) socket interface the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was the standard (and only) means to obtain network event indications.</span></span> <span data-ttu-id="ab0ef-105">Per ogni socket, è possibile eseguire il polling o l'attesa delle informazioni sullo stato di lettura, scrittura o errore.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-105">For each socket, information on read, write, or error status can be polled or waited on.</span></span> <span data-ttu-id="ab0ef-106">Per ulteriori informazioni, vedere [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab0ef-106">See [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) for more information.</span></span> <span data-ttu-id="ab0ef-107">Si noti che l'evento \_ di rete QoS FD non può essere ottenuto con questo approccio.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-107">Note that network event FD\_QOS cannot be obtained by this approach.</span></span>

 

 
