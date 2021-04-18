---
description: Poiché la DLL Winsock non è più fornita da ogni singolo fornitore dello stack, non è possibile che un fornitore di stack offra funzionalità estese aggiungendo punti di ingresso alla DLL Winsock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Meccanismo di estensione della funzione in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cfa6c9dfaf3afcec8e6861a9a0d3545a7ed0c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306980"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Meccanismo di estensione della funzione in SPI

Poiché la DLL Winsock non è più fornita da ogni singolo fornitore dello stack, non è possibile che un fornitore di stack offra funzionalità estese aggiungendo punti di ingresso alla DLL Winsock. Per ovviare a questa limitazione, Winsock sfrutta la nuova funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per ospitare i provider di servizi che desiderano offrire estensioni della funzionalità specifiche del provider. Questo meccanismo presuppone che un'applicazione sia in grado di riconoscere un'estensione specifica e conosca sia la semantica che la sintassi. Tali informazioni vengono in genere fornite dal fornitore del provider di servizi.

Per richiamare una funzione di estensione, l'applicazione deve innanzitutto richiedere un puntatore alla funzione desiderata. Questa operazione viene eseguita tramite la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando il \_ codice di comando del puntatore della funzione di estensione sio Get \_ \_ \_ . Il buffer di input per la funzione **WSAIoctl** contiene un identificatore per la funzione di estensione desiderata e il buffer di output conterrà il puntatore alla funzione stessa. L'applicazione può quindi richiamare la funzione di estensione direttamente senza passare attraverso la \_32.dll di WS2.

Gli identificatori assegnati alle funzioni di estensione sono identificatori univoci globali (GUID) allocati dai fornitori del provider di servizi. Ai fornitori che creano funzioni di estensione viene chiesto di pubblicare i dettagli completi sulla funzione, inclusa la sintassi del prototipo di funzione. Questo semplifica le funzioni di estensione comuni e/o più diffuse che possono essere offerte da più provider di servizi. Un'applicazione può ottenere il puntatore a funzione e utilizzare la funzione senza che sia necessario conoscere il particolare provider di servizi che implementa la funzione.

 

 



