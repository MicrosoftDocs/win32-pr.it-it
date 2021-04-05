---
description: WSPGetSockName viene utilizzato per recuperare l'indirizzo locale per i socket associati.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinazione dei nomi locali e remoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049488"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="d7187-103">Determinazione dei nomi locali e remoti</span><span class="sxs-lookup"><span data-stu-id="d7187-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="d7187-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) viene utilizzato per recuperare l'indirizzo locale per i socket associati.</span><span class="sxs-lookup"><span data-stu-id="d7187-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="d7187-105">Questa operazione è particolarmente utile quando viene effettuata una chiamata [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) senza eseguire prima un [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) ; **WSPGetSockName** fornisce l'unico mezzo per determinare l'associazione locale che è stata impostata in modo implicito dal provider.</span><span class="sxs-lookup"><span data-stu-id="d7187-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="d7187-106">Una volta configurata una connessione, è possibile usare [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) per determinare l'indirizzo del peer a cui è connesso un socket.</span><span class="sxs-lookup"><span data-stu-id="d7187-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
