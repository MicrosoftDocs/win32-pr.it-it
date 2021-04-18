---
description: Il contenuto degli annunci router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing. Le route non pubblicate vengono utilizzate per il routing, ma vengono ignorate durante la creazione di annunci router.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Annunci router IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310441"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="6bef1-104">Annunci router IPv6</span><span class="sxs-lookup"><span data-stu-id="6bef1-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="6bef1-105">Il contenuto degli annunci router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="6bef1-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="6bef1-106">Le route non pubblicate vengono utilizzate per il routing, ma vengono ignorate durante la creazione di annunci router.</span><span class="sxs-lookup"><span data-stu-id="6bef1-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="6bef1-107">Gli annunci router per IPv6 contengono sempre un'opzione relativa all'indirizzo del livello di collegamento di origine e un'opzione MTU.</span><span class="sxs-lookup"><span data-stu-id="6bef1-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="6bef1-108">Il valore dell'opzione MTU viene tratto dall'MTU del collegamento corrente dell'interfaccia mittente.</span><span class="sxs-lookup"><span data-stu-id="6bef1-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="6bef1-109">Questo valore può essere modificato con il comando IPv6 IFC.</span><span class="sxs-lookup"><span data-stu-id="6bef1-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="6bef1-110">L'annuncio router ha una durata di un router diverso da zero se è presente una route predefinita pubblicata.</span><span class="sxs-lookup"><span data-stu-id="6bef1-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="6bef1-111">Una route predefinita è una route per il prefisso di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="6bef1-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="6bef1-112">Le route di collegamento pubblicate generano le opzioni relative alle informazioni sul prefisso negli annunci router.</span><span class="sxs-lookup"><span data-stu-id="6bef1-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="6bef1-113">Se il prefisso on-link ha 64 bit, l'opzione relativa alle informazioni sul prefisso include sia il set di bit che gli host che lo ricevono. gli indirizzi vengono configurati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6bef1-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="6bef1-114">Un'interfaccia che invia annunci router consente anche di configurare automaticamente gli indirizzi in base alle opzioni di informazioni sul prefisso che invia.</span><span class="sxs-lookup"><span data-stu-id="6bef1-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="6bef1-115">Si consiglia di usare una durata di non invecchiamento finita in tutte le route pubblicate, ad esempio 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="6bef1-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="6bef1-116">Se si decide di ritirare una route, è possibile modificare la route in modo che abbia una durata di invecchiamento.</span><span class="sxs-lookup"><span data-stu-id="6bef1-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="6bef1-117">La route sarà di età nel corso di diversi annunci router e quindi scomparirà sia dal router che dagli host che ricevono gli annunci del router.</span><span class="sxs-lookup"><span data-stu-id="6bef1-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="6bef1-118">Le route che gli host trovano tramite gli annunci router Age e non vengono pubblicate.</span><span class="sxs-lookup"><span data-stu-id="6bef1-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="6bef1-119">Indirizzi configurati automaticamente dall'età degli annunci router.</span><span class="sxs-lookup"><span data-stu-id="6bef1-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



