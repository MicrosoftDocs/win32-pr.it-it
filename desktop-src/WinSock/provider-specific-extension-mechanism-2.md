---
description: La funzione WSAIoctl consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Meccanismo di estensione Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58a8bba3c83e7dbf973ff8fe5b7d91c1065cfc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129130"
---
# <a name="provider-specific-extension-mechanism"></a>Meccanismo di estensione Provider-Specific

La funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider. Questo meccanismo presuppone, ovviamente, che un'applicazione sia in grado di riconoscere un'estensione specifica e conosca sia la semantica che la sintassi. Tali informazioni vengono in genere fornite dal fornitore del provider di servizi.

Per richiamare una funzione di estensione, l'applicazione deve innanzitutto richiedere un puntatore alla funzione desiderata. Questa operazione viene eseguita tramite la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando il \_ codice di comando del puntatore della funzione di estensione sio Get \_ \_ \_ . Il buffer di input per **WSAIoctl** contiene un identificatore per la funzione di estensione desiderata mentre il buffer di output contiene il puntatore alla funzione stessa. L'applicazione può quindi richiamare la funzione di estensione direttamente senza passare attraverso la \_32.dll di WS2.

Gli identificatori assegnati alle funzioni di estensione sono identificatori univoci globali (GUID) allocati dai fornitori del provider di servizi. Ai fornitori che creano funzioni di estensione viene chiesto di pubblicare i dettagli completi sulla funzione, inclusa la sintassi del prototipo di funzione. In questo modo è possibile che le funzioni di estensione comuni e più diffuse siano offerte da più fornitori del provider di servizi. Un'applicazione può ottenere il puntatore a funzione e utilizzare la funzione senza che sia necessario conoscere il particolare provider di servizi che implementa la funzione.

In Windows Vista e versioni successive, le nuove estensioni di sistema Winsock vengono esportate direttamente dalla DLL Winsock, quindi la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) non è necessaria per caricare queste estensioni. Le nuove funzioni di estensione disponibili in Windows Vista e versioni successive includono le funzioni [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) esportate da *WS2 \_32.dll*.

 

 
