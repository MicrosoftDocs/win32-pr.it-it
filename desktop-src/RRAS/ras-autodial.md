---
title: Autodial RAS
description: Funzionalità denominata \ 0034; connessione predefinita \ 0034; è stato aggiunto al sistema in Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Autodial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298809"
---
# <a name="ras-autodial"></a><span data-ttu-id="e9711-104">Autodial RAS</span><span class="sxs-lookup"><span data-stu-id="e9711-104">RAS AutoDial</span></span>

<span data-ttu-id="e9711-105">Una funzionalità denominata "connessione predefinita" è stata aggiunta al sistema in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9711-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="e9711-106">Se si verifica un tentativo di connessione non riuscito, il sistema verifica la presenza di una corrispondenza esplicita (per nome o nome di condivisione Winsock) nel database, in caso contrario, compone la connessione predefinita se presente.</span><span class="sxs-lookup"><span data-stu-id="e9711-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="e9711-107">**Windows 2000:** Quando un tentativo di connessione a un indirizzo di rete non riesce perché non è possibile raggiungere l'host, la funzionalità Autodial può avviare automaticamente un'operazione di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e9711-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="e9711-108">A tale scopo, Autodial Cerca nel database gli indirizzi di rete per trovare una voce di rubrica che può usare per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="e9711-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="e9711-109">**Windows NT 4,0:  ** RAS mantiene un database dei nomi e/o delle condivisioni Winsock che sono stati raggiunti correttamente mentre era attiva una connessione RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="e9711-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="e9711-110">In un secondo momento, quando un tentativo di connessione Winsock o condivisione non riesce, il sistema controlla questo database e offre la connessione automatica alla connessione archiviata.</span><span class="sxs-lookup"><span data-stu-id="e9711-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




