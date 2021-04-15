---
description: Un utente può verificare lo stato dell'interfaccia Teredo dal prompt dei comandi digitando netsh interface teredo show state ed esaminando l'output.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Infrastruttura peer e Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529119"
---
# <a name="the-peer-infrastructure-and-teredo"></a><span data-ttu-id="3e35d-103">Infrastruttura peer e Teredo</span><span class="sxs-lookup"><span data-stu-id="3e35d-103">The Peer Infrastructure and Teredo</span></span>

<span data-ttu-id="3e35d-104">Un utente può verificare lo stato dell'interfaccia [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) dal prompt dei comandi digitando **netsh interface teredo show state** ed esaminando l'output.</span><span class="sxs-lookup"><span data-stu-id="3e35d-104">A user can check the status of the [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) interface from the command prompt by typing **netsh interface teredo show state** and examining the output.</span></span> <span data-ttu-id="3e35d-105">Se lo stato è "offline", Teredo non è attivo, che impedisce all'utente di connettersi ad altri utenti tramite i rispettivi indirizzi Teredo.</span><span class="sxs-lookup"><span data-stu-id="3e35d-105">If the state is "offline", Teredo is not active, which prevents the user from connecting to other users via their Teredo addresses.</span></span> <span data-ttu-id="3e35d-106">È possibile che Teredo sia offline perché il firewall è disabilitato o non supporta [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="3e35d-106">It is possible Teredo may be offline because your firewall is disabled or does not support [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span></span>

 

 
