---
description: La destinazione predefinita può essere modificata semplicemente chiamando di nuovo WSPConnect, anche se il socket è già connesso. Eventuali datagrammi in coda per la ricezione vengono eliminati se il nuovo indirizzo è diverso dall'indirizzo specificato in una WSPConnect precedente.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Riconnessione e disconnessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880686"
---
# <a name="reconnecting-and-disconnecting"></a>Riconnessione e disconnessione

La destinazione predefinita può essere modificata semplicemente chiamando di nuovo [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , anche se il socket è già connesso. Eventuali datagrammi in coda per la ricezione vengono eliminati se il nuovo indirizzo è diverso dall'indirizzo specificato in una **WSPConnect** precedente.

Se l'indirizzo specificato per il socket è costituito da tutti zeri, il socket verrà disconnesso. l'indirizzo remoto predefinito sarà indeterminato, quindi le chiamate [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) restituiranno il codice di errore WSAENOTCONN, sebbene sia possibile utilizzare [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) .

 

 
