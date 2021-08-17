---
description: Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Segnalazione errori e convalida dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132614"
---
# <a name="error-reporting-and-parameter-validation"></a>Segnalazione errori e convalida dei parametri

Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API. Windows I provider di servizi Sockets segnalano errori insieme alla funzione restituita, anziché l'approccio basato su thread utilizzato nell'API. L'32.dll Ws2 usa il codice di errore per funzione del provider di servizi per aggiornare il valore di errore per thread ottenuto tramite la funzione \_ API [**WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) I provider di servizi sono comunque necessari per mantenere l'errore basato su socket che può essere recuperato tramite l'opzione socket SO \_ ERROR.

L'32.dll Ws2 esegue la convalida dei parametri solo per le chiamate \_ di funzione implementate interamente all'interno di se stessa. I provider di servizi sono responsabili dell'esecuzione di tutte le proprie operazioni di convalida dei parametri.

 

 



