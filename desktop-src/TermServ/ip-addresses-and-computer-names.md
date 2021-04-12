---
title: Indirizzi IP e nomi di computer
description: Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338887"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="4fe8c-103">Indirizzi IP e nomi di computer</span><span class="sxs-lookup"><span data-stu-id="4fe8c-103">IP addresses and computer names</span></span>

<span data-ttu-id="4fe8c-104">È possibile eseguire l'accesso simultaneo a più utenti a un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="4fe8c-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="4fe8c-105">Di conseguenza, non è sicuro presupporre che il nome del computer o l'indirizzo IP assegnato al computer siano associati a un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="4fe8c-106">Questo comportamento è diverso da un ambiente Windows a utente singolo, in cui solo un utente è connesso alla volta.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="4fe8c-107">Le applicazioni che utilizzano il nome del computer o l'indirizzo IP per la gestione delle licenze o come mezzo per identificare un'iterazione dell'applicazione nella rete non funzioneranno correttamente in un ambiente di Servizi Desktop remoto, perché il nome del computer o l'indirizzo IP del server può essere associato a molti utenti.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="4fe8c-108">In un ambiente di Servizi Desktop remoto, ogni terminale client o emulatore di terminale ha un indirizzo IP e un nome computer distinti.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="4fe8c-109">Per recuperare l'indirizzo IP e il nome computer di un client, chiamare la funzione [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="4fe8c-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="4fe8c-110">Altre funzioni che recuperano questi indirizzi di rete e nomi di computer recuperano il nome e l'indirizzo del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="4fe8c-111">Ad esempio, la funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) restituisce il nome computer del server.</span><span class="sxs-lookup"><span data-stu-id="4fe8c-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 