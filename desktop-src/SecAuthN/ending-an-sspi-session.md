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
# <a name="ending-an-sspi-session"></a>Chiusura di una sessione SSPI

Al termine della comunicazione tra il client e il server, entrambi i lati chiamano la funzione [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con i rispettivi handle di contesto. Quando il client ha terminato la comunicazione con qualsiasi server o ha terminato l'uso delle credenziali aggiuntive passate alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , il client deve chiamare la funzione [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Quando il server è pronto per l'arresto e prima dello scaricamento della DLL, il server deve chiamare **DeleteSecurityContext**.

 

 
