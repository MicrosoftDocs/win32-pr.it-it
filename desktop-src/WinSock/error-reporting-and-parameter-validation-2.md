---
description: Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Segnalazione errori e convalida parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306989"
---
# <a name="error-reporting-and-parameter-validation"></a>Segnalazione errori e convalida parametri

Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API. I provider di servizi Windows Sockets segnalano gli errori insieme alla funzione che restituisce, anziché l'approccio basato sui singoli thread usato nell'API. Il \_32.dll WS2 usa il codice di errore per funzione del provider di servizi per aggiornare il valore di errore per thread ottenuto tramite la funzione API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Tuttavia, i provider di servizi sono ancora necessari per gestire l'errore basato sui socket, che può essere recuperato tramite l' \_ opzione del socket di errore so.

Il \_32.dll WS2 esegue la convalida dei parametri solo per le chiamate di funzione implementate interamente all'interno di se stesso. I provider di servizi sono responsabili dell'esecuzione di tutta la relativa convalida dei parametri.

 

 



