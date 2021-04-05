---
description: Quando il client ha terminato la comunicazione con qualsiasi server o ha terminato l'uso delle credenziali aggiuntive passate alla funzione AcquireCredentialsHandle, il client deve chiamare la funzione FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Chiusura di una sessione SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750930"
---
# <a name="ending-an-sspi-session"></a><span data-ttu-id="cdf40-103">Chiusura di una sessione SSPI</span><span class="sxs-lookup"><span data-stu-id="cdf40-103">Ending an SSPI Session</span></span>

<span data-ttu-id="cdf40-104">Al termine della comunicazione tra il client e il server, entrambi i lati chiamano la funzione [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con i rispettivi handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="cdf40-104">After the client and server have finished communicating, both sides call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function with their respective context handles.</span></span> <span data-ttu-id="cdf40-105">Quando il client ha terminato la comunicazione con qualsiasi server o ha terminato l'uso delle credenziali aggiuntive passate alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , il client deve chiamare la funzione [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="cdf40-105">When the client has finished communicating with any server or has finished using the additional credentials passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, the client must call the [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) function.</span></span> <span data-ttu-id="cdf40-106">Quando il server è pronto per l'arresto e prima dello scaricamento della DLL, il server deve chiamare **DeleteSecurityContext**.</span><span class="sxs-lookup"><span data-stu-id="cdf40-106">When the server is ready to shut down and before unloading the DLL, the server must call **DeleteSecurityContext**.</span></span>

 

 
