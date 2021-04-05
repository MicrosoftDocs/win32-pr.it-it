---
description: Network Monitor fornisce una struttura PROPERTYINFO per definire le proprietà di un protocollo e una struttura PROPERTYINST e PROPERTYINSTEX per definire un'istanza di una proprietà.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definizione di proprietà e strutture dell'istanza di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756210"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="fdff8-103">Definizione di proprietà e strutture dell'istanza di proprietà</span><span class="sxs-lookup"><span data-stu-id="fdff8-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="fdff8-104">Network Monitor fornisce una struttura [**PROPERTYINFO**](propertyinfo.md) per definire le proprietà di un protocollo e una struttura [**PROPERTYINST**](propertyinst.md)e [**PROPERTYINSTEX**](propertyinstex.md) per definire un'istanza di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="fdff8-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![strutture di Network Monitor](images/property1.png)

<span data-ttu-id="fdff8-106">Il parser alloca e compila la struttura [**PROPERTYINFO**](propertyinfo.md) per tutte le proprietà supportate da un protocollo.</span><span class="sxs-lookup"><span data-stu-id="fdff8-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="fdff8-107">Il parser passa la struttura a Network Monitor dove la struttura viene aggiunta al database della [*Proprietà*](p.md)del protocollo.</span><span class="sxs-lookup"><span data-stu-id="fdff8-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="fdff8-108">Le informazioni contenute nella struttura **PROPERTYINFO** vengono utilizzate durante l'analisi di un'istanza di una proprietà e durante la formattazione dei dati visualizzati nell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="fdff8-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="fdff8-109">Network Monitor alloca le strutture [**PROPERTYINST**](propertyinst.md) e [**PROPERTYINSTEX**](propertyinstex.md) quando il parser connette una definizione di proprietà a un'istanza di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="fdff8-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="fdff8-110">Nella procedura seguente vengono identificati i passaggi necessari per alleghire una definizione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fdff8-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="fdff8-111">**Per alleghi una definizione di proprietà**</span><span class="sxs-lookup"><span data-stu-id="fdff8-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="fdff8-112">Identificare ogni proprietà presente in un'istanza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="fdff8-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="fdff8-113">Quando si aggiunge una definizione, Network Monitor passa i dati acquisiti al parser.</span><span class="sxs-lookup"><span data-stu-id="fdff8-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="fdff8-114">I dati vengono passati in base a un'istanza di protocollo.</span><span class="sxs-lookup"><span data-stu-id="fdff8-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="fdff8-115">Determinare il percorso della proprietà nell'istanza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="fdff8-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="fdff8-116">Alleghi una definizione di proprietà al percorso della proprietà.</span><span class="sxs-lookup"><span data-stu-id="fdff8-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="fdff8-117">Network Monitor implementa una struttura [**PROPERTYINST**](propertyinst.md) quando il parser usa i dati della proprietà così come esistono nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="fdff8-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="fdff8-118">Network Monitor implementa una struttura [**PROPERTYINSTEX**](propertyinstex.md) quando il parser deve modificare i dati della proprietà nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="fdff8-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



