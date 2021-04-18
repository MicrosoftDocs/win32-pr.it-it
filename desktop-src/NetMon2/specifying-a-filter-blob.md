---
description: Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile utilizzare un BLOB di filtro per ignorare le NIC a cui non si è interessati.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Specifica di un BLOB di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307706"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="f95b5-103">Specifica di un BLOB di filtro</span><span class="sxs-lookup"><span data-stu-id="f95b5-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="f95b5-104">Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile utilizzare un [*BLOB di filtro*](f.md) per ignorare le NIC a cui non si è interessati.</span><span class="sxs-lookup"><span data-stu-id="f95b5-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="f95b5-105">Ad esempio, è possibile limitare la ricerca di un tipo specifico di scheda (ad esempio ETHERNET) o di un indirizzo MAC specifico.</span><span class="sxs-lookup"><span data-stu-id="f95b5-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="f95b5-106">Durante la ricerca di una scheda di interfaccia di rete, ogni voce nel BLOB di filtro deve corrispondere a una voce equivalente nel BLOB di NPP che rappresenta la scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f95b5-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="f95b5-107">I BLOB di filtro possono anche essere [*BLOB speciali*](s.md).</span><span class="sxs-lookup"><span data-stu-id="f95b5-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="f95b5-108">Quando viene chiamata la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , il BLOB di filtro limita le schede di rete visualizzate nella finestra di dialogo **Seleziona una rete** .</span><span class="sxs-lookup"><span data-stu-id="f95b5-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="f95b5-109">Quando viene chiamata la funzione [**GetNPPBlobTable**](getnppblobtable.md) , il BLOB di filtro limita le schede di rete restituite nella tabella BLOB.</span><span class="sxs-lookup"><span data-stu-id="f95b5-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="f95b5-110">Per usare il filtro, è necessario creare un BLOB di filtro, impostare i valori delle proprietà su cui applicare il filtro (incluse eventuali voci di BLOB speciali), quindi specificare il filtro BLOB e una chiamata alla funzione [**GetNPPBlobTable**](getnppblobtable.md) o [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="f95b5-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="f95b5-111">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="f95b5-111">For information on</span></span>                                 | <span data-ttu-id="f95b5-112">Vedere</span><span class="sxs-lookup"><span data-stu-id="f95b5-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95b5-113">Come selezionare una scheda di interfaccia di rete registrata in un computer locale</span><span class="sxs-lookup"><span data-stu-id="f95b5-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="f95b5-114">Selezione di una scheda di interfaccia di rete registrata</span><span class="sxs-lookup"><span data-stu-id="f95b5-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="f95b5-115">Recupero di una tabella BLOB di NPP</span><span class="sxs-lookup"><span data-stu-id="f95b5-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="f95b5-116">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita</span><span class="sxs-lookup"><span data-stu-id="f95b5-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



