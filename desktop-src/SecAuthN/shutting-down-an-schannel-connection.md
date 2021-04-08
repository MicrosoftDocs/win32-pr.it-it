---
description: Chiusura di una connessione Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Chiusura di una connessione Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749602"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="20e72-103">Chiusura di una connessione Schannel</span><span class="sxs-lookup"><span data-stu-id="20e72-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="20e72-104">Al termine della connessione, un client o un server deve arrestarlo.</span><span class="sxs-lookup"><span data-stu-id="20e72-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="20e72-105">L'altra parte, a sua volta, deve riconoscere l'arresto ed eliminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="20e72-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="20e72-106">**Per arrestare una connessione Schannel**</span><span class="sxs-lookup"><span data-stu-id="20e72-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="20e72-107">Chiamare la funzione [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , specificando il \_ token di controllo di arresto di Schannel.</span><span class="sxs-lookup"><span data-stu-id="20e72-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="20e72-108">Dopo \_ la ricezione di un \_ valore restituito sec E OK da [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), chiamare la funzione [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) o [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), passando i buffer vuoti.</span><span class="sxs-lookup"><span data-stu-id="20e72-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="20e72-109">Continuare come se l'applicazione creasse una nuova connessione fino a quando la funzione restituisce il \_ contesto di secondo i non \_ \_ scaduto o sec \_ E \_ OK per indicare che la connessione è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="20e72-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="20e72-110">Inviare le informazioni di output finale, se presenti, alla parte remota.</span><span class="sxs-lookup"><span data-stu-id="20e72-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="20e72-111">Chiamare [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) per liberare risorse detenute dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="20e72-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="20e72-112">Riconoscimento di un arresto</span><span class="sxs-lookup"><span data-stu-id="20e72-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="20e72-113">La funzione [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) restituisce il \_ contesto di sec i \_ \_ scaduto quando il mittente del messaggio chiude la connessione.</span><span class="sxs-lookup"><span data-stu-id="20e72-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="20e72-114">Dopo la ricezione del valore restituito, attenersi alla procedura per arrestare una connessione Schannel, più indietro in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="20e72-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
