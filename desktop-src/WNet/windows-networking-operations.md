---
title: Operazioni di rete di Windows
description: Un'applicazione può utilizzare le funzioni WNet per esplorare, aggiungere o annullare le connessioni di rete in qualsiasi punto della gerarchia di rete.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337919"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="c3be9-103">Operazioni di rete di Windows</span><span class="sxs-lookup"><span data-stu-id="c3be9-103">Windows Networking Operations</span></span>

<span data-ttu-id="c3be9-104">Un'applicazione può utilizzare le funzioni WNet per esplorare, aggiungere o annullare le connessioni di rete in qualsiasi punto della gerarchia di rete.</span><span class="sxs-lookup"><span data-stu-id="c3be9-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="c3be9-105">Una *connessione permanente* è una connessione di rete ripristinata automaticamente dal sistema quando l'utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="c3be9-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="c3be9-106">È possibile chiamare le funzioni [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) per controllare se una connessione di rete è permanente da una sessione a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="c3be9-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="c3be9-107">Per trovare il nome utente predefinito o il nome utente utilizzato per stabilire una connessione di rete, chiamare la funzione [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="c3be9-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="c3be9-108">Oltre a chiamare le funzioni WNet, un processo può utilizzare anche mailslot e named pipe per comunicare con un altro processo.</span><span class="sxs-lookup"><span data-stu-id="c3be9-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="c3be9-109">Per altre informazioni, vedere [mailslot](/windows/desktop/ipc/mailslots) e [Pipes](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="c3be9-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 