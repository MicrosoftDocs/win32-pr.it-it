---
title: Informazioni sulla rete di Windows
description: Le applicazioni possono utilizzare le funzioni WNet per aggiungere e annullare le connessioni di rete e recuperare informazioni sulla configurazione corrente della rete.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows Networking WNet, descritto
- WNet WNet, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045320"
---
# <a name="about-windows-networking"></a><span data-ttu-id="efa77-105">Informazioni sulla rete di Windows</span><span class="sxs-lookup"><span data-stu-id="efa77-105">About Windows Networking</span></span>

<span data-ttu-id="efa77-106">Le applicazioni possono utilizzare le funzioni WNet per aggiungere e annullare le connessioni di rete e recuperare informazioni sulla configurazione corrente della rete.</span><span class="sxs-lookup"><span data-stu-id="efa77-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="efa77-107">Nella figura seguente viene illustrata la struttura di una rete tipica.</span><span class="sxs-lookup"><span data-stu-id="efa77-107">The following figure shows the structure of a typical network.</span></span>

![struttura di rete tipica](images/csnet-01.png)

<span data-ttu-id="efa77-109">Nella figura precedente, la gerarchia per le risorse di Windows NT Server/Windows 2000 Server è fornita in dettaglio come provider di rete \# 1.</span><span class="sxs-lookup"><span data-stu-id="efa77-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="efa77-110">Le risorse di rete di altri provider hanno sistemi gerarchici diversi.</span><span class="sxs-lookup"><span data-stu-id="efa77-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="efa77-111">Un'applicazione non necessita di informazioni sulla gerarchia prima che inizi a funzionare con una rete.</span><span class="sxs-lookup"><span data-stu-id="efa77-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="efa77-112">Può procedere dalla radice di rete (ovvero la risorsa del contenitore più in alto) e recuperare le informazioni sulle risorse della rete in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="efa77-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="efa77-113">Le risorse di rete che contengono altre risorse sono denominate *contenitori*.</span><span class="sxs-lookup"><span data-stu-id="efa77-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="efa77-114">Le risorse del contenitore sono incluse nelle caselle della figura precedente.</span><span class="sxs-lookup"><span data-stu-id="efa77-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="efa77-115">Le risorse che non contengono altre risorse sono denominate *oggetti*.</span><span class="sxs-lookup"><span data-stu-id="efa77-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="efa77-116">Nella figura precedente, SharePoint \# 1 e SharePoint \# 2 sono oggetti.</span><span class="sxs-lookup"><span data-stu-id="efa77-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="efa77-117">*SharePoint* è un oggetto accessibile attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="efa77-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="efa77-118">Esempi di SharePoint includono stampanti e directory condivise.</span><span class="sxs-lookup"><span data-stu-id="efa77-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




