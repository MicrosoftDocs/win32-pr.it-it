---
description: Per selezionare una delle schede di rete registrate nel computer locale, chiamare la funzione GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selezione di una scheda di interfaccia di rete registrata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310490"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="f0d92-103">Selezione di una scheda di interfaccia di rete registrata</span><span class="sxs-lookup"><span data-stu-id="f0d92-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="f0d92-104">Per selezionare una delle schede di rete registrate nel computer locale, chiamare la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d92-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="f0d92-105">Questa funzione usa l'interfaccia utente di Network Monitor per visualizzare le schede di interfaccia di rete registrate e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete selezionata.</span><span class="sxs-lookup"><span data-stu-id="f0d92-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="f0d92-106">È possibile visualizzare tutte le schede di rete registrate nel computer locale o un set più piccolo di schede di rete filtrate.</span><span class="sxs-lookup"><span data-stu-id="f0d92-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="f0d92-107">Per filtrare le NIC visualizzate, fornire un [*BLOB di filtro*](f.md) quando viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0d92-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="f0d92-108">Quando viene chiamata la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , il [*Finder di NPP*](n.md) comunica con le DLL di NPP per ottenere le strutture BLOB di NPP che rappresentano le schede NIC registrate.</span><span class="sxs-lookup"><span data-stu-id="f0d92-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="f0d92-109">Per ulteriori informazioni e per una procedura su come utilizzare direttamente l'interfaccia utente di Network Monitor, vedere l'argomento "selezionare una rete nella finestra di dialogo" nella Guida in linea di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="f0d92-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="f0d92-110">Quando si chiama la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , viene visualizzata la finestra **di dialogo selezionare una rete** .</span><span class="sxs-lookup"><span data-stu-id="f0d92-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="f0d92-111">È possibile visualizzare i dettagli di centrali registrati nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="f0d92-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="f0d92-112">Queste informazioni includono sia centrali locale che centrali remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d92-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="f0d92-113">Nella finestra di dialogo è possibile selezionare una scheda di interfaccia di rete specifica e visualizzare i dettagli della struttura del BLOB di NPP associata.</span><span class="sxs-lookup"><span data-stu-id="f0d92-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="f0d92-114">Nella figura seguente sono illustrate le impostazioni tipiche di una NPP di tipo NDIS fornita da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="f0d92-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![impostazioni tipiche di una NPP di tipo NDIS fornita da Network Monitor](images/networkdb.png)

<span data-ttu-id="f0d92-116">Nella tabella seguente sono elencati gli argomenti che descrivono ogni metodo di selezione NIC.</span><span class="sxs-lookup"><span data-stu-id="f0d92-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="f0d92-117">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="f0d92-117">For information about</span></span>                                                                          | <span data-ttu-id="f0d92-118">Vedere</span><span class="sxs-lookup"><span data-stu-id="f0d92-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d92-119">Come specificare un filtro che limita le NIC visualizzate nella finestra di dialogo **Seleziona rete** .</span><span class="sxs-lookup"><span data-stu-id="f0d92-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="f0d92-120">Specifica di un BLOB di filtro</span><span class="sxs-lookup"><span data-stu-id="f0d92-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="f0d92-121">Come selezionare una scheda di interfaccia di rete chiamando la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d92-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="f0d92-122">Selezione di una scheda di interfaccia di rete con GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="f0d92-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="f0d92-123">Come selezionare una scheda di interfaccia di rete da una tabella BLOB NPP specificata.</span><span class="sxs-lookup"><span data-stu-id="f0d92-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="f0d92-124">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata</span><span class="sxs-lookup"><span data-stu-id="f0d92-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



