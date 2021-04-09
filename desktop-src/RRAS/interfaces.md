---
title: Interfacce RAS
description: Un'interfaccia rappresenta una rete che può essere raggiunta tramite un adapter LAN o WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857834"
---
# <a name="ras-interfaces"></a><span data-ttu-id="6af41-103">Interfacce RAS</span><span class="sxs-lookup"><span data-stu-id="6af41-103">RAS interfaces</span></span>

<span data-ttu-id="6af41-104">Un'interfaccia rappresenta una rete che può essere raggiunta tramite un adapter LAN o WAN.</span><span class="sxs-lookup"><span data-stu-id="6af41-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="6af41-105">Ogni interfaccia ha un identificatore univoco sul router.</span><span class="sxs-lookup"><span data-stu-id="6af41-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="6af41-106">Le interfacce attive hanno un adapter che fornisce la connettività alla rete che rappresentano.</span><span class="sxs-lookup"><span data-stu-id="6af41-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="6af41-107">Le interfacce inattive non dispongono di un adapter che fornisce la connettività, a meno che un amministratore non abbia disabilitato l'interfaccia dopo che era già presente un adapter.</span><span class="sxs-lookup"><span data-stu-id="6af41-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="6af41-108">Il routing di un pacchetto a una rete rappresentata da un'interfaccia provocherà l'allocazione di un adapter per l'interfaccia da parte del router e la connessione WAN alla rete remota.</span><span class="sxs-lookup"><span data-stu-id="6af41-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="6af41-109">L'allocazione di un adapter a un'interfaccia viene definita *Binding*.</span><span class="sxs-lookup"><span data-stu-id="6af41-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="6af41-110">Le interfacce sono oggetti gestibili.</span><span class="sxs-lookup"><span data-stu-id="6af41-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="6af41-111">Ogni interfaccia viene visualizzata come riga nella tabella di interfaccia del MIB SNMP appropriato.</span><span class="sxs-lookup"><span data-stu-id="6af41-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>