---
description: Net.exe può essere utilizzato per arrestare e avviare il protocollo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879197"
---
# <a name="netexe"></a><span data-ttu-id="b10b0-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="b10b0-103">Net.exe</span></span>

<span data-ttu-id="b10b0-104">Net.exe può essere utilizzato per arrestare e avviare il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="b10b0-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="b10b0-105">Il riavvio di IPv6 reinizializza il protocollo come se il computer venisse riavviato, il che potrebbe modificare i numeri di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b10b0-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="b10b0-106">Net.exe dispone di molti sottocomandi.</span><span class="sxs-lookup"><span data-stu-id="b10b0-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="b10b0-107">I comandi seguenti sono rilevanti per IPv6:</span><span class="sxs-lookup"><span data-stu-id="b10b0-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="b10b0-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET STOP tcpip6**</span><span class="sxs-lookup"><span data-stu-id="b10b0-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="b10b0-109">Arresta il protocollo IPv6 e lo Scarica dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="b10b0-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="b10b0-110">Questo comando non riesce se sono presenti socket IPv6 aperti.</span><span class="sxs-lookup"><span data-stu-id="b10b0-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="b10b0-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET Start tcpip6**</span><span class="sxs-lookup"><span data-stu-id="b10b0-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="b10b0-112">Avvia il protocollo IPv6 se è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="b10b0-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="b10b0-113">Se nella directory% SystemRoot% system32 drivers è presente un nuovo file di driver Tcpip6.sys \\ \\ , viene caricato il file del driver.</span><span class="sxs-lookup"><span data-stu-id="b10b0-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



