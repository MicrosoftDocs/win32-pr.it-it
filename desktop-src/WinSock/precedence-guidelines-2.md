---
description: I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Linee guida per la precedenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129138"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="6fd85-103">Linee guida per la precedenza</span><span class="sxs-lookup"><span data-stu-id="6fd85-103">Precedence Guidelines</span></span>

<span data-ttu-id="6fd85-104">I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O.</span><span class="sxs-lookup"><span data-stu-id="6fd85-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="6fd85-105">Tuttavia, l'interfaccia Windows Sockets non implementa alcun tipo di controllo di accesso, quindi spetta ai processi che coordinano le operazioni su un socket condiviso.</span><span class="sxs-lookup"><span data-stu-id="6fd85-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="6fd85-106">Un utilizzo tipico per i socket condivisi consiste nel disporre di un processo responsabile della creazione di socket e della creazione di connessioni che trasferiscono i socket ad altri processi responsabili dello scambio di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6fd85-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="6fd85-107">La linea guida generale per il supporto di più operazioni in attesa sui socket condivisi è che un provider di servizi è incoraggiato a rispettare tutte le operazioni simultanee sui socket condivisi, in particolare l'operazione più recente su un oggetto Socket.</span><span class="sxs-lookup"><span data-stu-id="6fd85-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="6fd85-108">Se necessario, questo può verificarsi a scapito dell'annullamento di alcune delle operazioni precedenti, ma ancora in sospeso, che restituiranno WSAEINTR in questo caso.</span><span class="sxs-lookup"><span data-stu-id="6fd85-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



