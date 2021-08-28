---
description: La funzione WSAIoctl consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific meccanismo di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733571"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific meccanismo di estensione

La [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) consente ai provider di servizi di offrire estensioni di funzionalità specifiche del provider. Questo meccanismo presuppone, naturalmente, che un'applicazione sia a conoscenza di una determinata estensione e comprendi sia la semantica che la sintassi coinvolte. Tali informazioni vengono in genere fornite dal fornitore del provider di servizi.

Per richiamare una funzione di estensione, l'applicazione deve prima richiedere un puntatore alla funzione desiderata. Questa operazione viene eseguita tramite la [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando il codice di comando SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER. Il buffer di input **per WSAIoctl** contiene un identificatore per la funzione di estensione desiderata, mentre il buffer di output contiene il puntatore a funzione stesso. L'applicazione può quindi richiamare direttamente la funzione di estensione senza passare attraverso il32.dll \_ Ws2.

Gli identificatori assegnati alle funzioni di estensione sono identificatori univoci globali (GUID) allocati dai fornitori di provider di servizi. I fornitori che creano funzioni di estensione sono invitati a pubblicare dettagli completi sulla funzione, inclusa la sintassi del prototipo di funzione. Ciò consente a più fornitori di provider di servizi di offrire funzioni di estensione comuni e più comuni. Un'applicazione può ottenere il puntatore a funzione e usare la funzione senza dover conoscere il provider di servizi specifico che implementa la funzione.

In Windows Vista e versioni successive, le nuove estensioni di sistema Winsock vengono esportate direttamente dalla DLL Winsock, quindi la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) non è necessaria per caricare queste estensioni. Le nuove funzioni di estensione disponibili in Windows Vista e versioni successive includono le funzioni [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) esportate da *Ws2 \_32.dll*.

 

 
