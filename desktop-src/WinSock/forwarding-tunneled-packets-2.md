---
description: Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneling) e li demultiplexi a un'interfaccia specifica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Pacchetti con tunneling di inoltri IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879213"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="214df-103">Pacchetti con tunneling di inoltri IPv6</span><span class="sxs-lookup"><span data-stu-id="214df-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="214df-104">Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneling) e li demultiplexi a un'interfaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="214df-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="214df-105">Se si vuole inoltrare i pacchetti con tunneling ricevuti tramite un tunnel configurato, è necessario abilitare l'inoltramento su tutte le interfacce 6-over-4 e sull'interfaccia \# 2.</span><span class="sxs-lookup"><span data-stu-id="214df-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="214df-106">L'abilitazione dell'invio solo sull'interfaccia \# 2 non funziona.</span><span class="sxs-lookup"><span data-stu-id="214df-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="214df-107">In genere, quando si configura un router, si Abilita l'invio in tutte le interfacce ad eccezione di loopback.</span><span class="sxs-lookup"><span data-stu-id="214df-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



