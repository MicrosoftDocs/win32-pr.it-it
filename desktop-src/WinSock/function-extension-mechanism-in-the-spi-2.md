---
description: Poiché la DLL winsock non viene più fornita da ogni singolo fornitore di stack, non è possibile per un fornitore di stack offrire funzionalità estese aggiungendo punti di ingresso alla DLL Winsock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Meccanismo di estensione della funzione in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2e5e32a4d79174893cfb2d9fa2ae0c0521a51ac80c40bcb6c45feab49693d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132424"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Meccanismo di estensione della funzione in SPI

Poiché la DLL winsock non viene più fornita da ogni singolo fornitore di stack, non è possibile per un fornitore di stack offrire funzionalità estese aggiungendo punti di ingresso alla DLL Winsock. Per superare questa limitazione, Winsock sfrutta la nuova funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per supportare i provider di servizi che vogliono offrire estensioni di funzionalità specifiche del provider. Questo meccanismo presuppone che un'applicazione sia a conoscenza di una determinata estensione e comprendi sia la semantica che la sintassi coinvolte. Tali informazioni vengono in genere fornite dal fornitore del provider di servizi.

Per richiamare una funzione di estensione, l'applicazione deve prima richiedere un puntatore alla funzione desiderata. Questa operazione viene eseguita tramite la [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando il codice di comando SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER. Il buffer di input per **la funzione WSAIoctl** contiene un identificatore per la funzione di estensione desiderata e il buffer di output conterrà il puntatore a funzione stesso. L'applicazione può quindi richiamare direttamente la funzione di estensione senza passare attraverso il32.dll \_ Ws2.

Gli identificatori assegnati alle funzioni di estensione sono identificatori univoci globali (GUID) allocati dai fornitori di provider di servizi. I fornitori che creano funzioni di estensione sono autorizzati a pubblicare dettagli completi sulla funzione, inclusa la sintassi del prototipo di funzione. In questo modo, le funzioni di estensione comuni e/o più comuni possono essere offerte da più provider di servizi. Un'applicazione può ottenere il puntatore a funzione e usare la funzione senza dover conoscere il provider di servizi specifico che implementa la funzione.

 

 



