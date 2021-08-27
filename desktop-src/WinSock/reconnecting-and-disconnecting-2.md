---
description: La destinazione predefinita può essere modificata semplicemente chiamando di nuovo WSPConnect, anche se il socket è già connesso. Eventuali datagrammi accodati per la ricezione vengono eliminati se il nuovo indirizzo è diverso dall'indirizzo specificato in un WSPConnect precedente.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Riconnessione e disconnessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121361"
---
# <a name="reconnecting-and-disconnecting"></a>Riconnessione e disconnessione

La destinazione predefinita può essere modificata semplicemente chiamando di nuovo [**WSPConnect,**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) anche se il socket è già connesso. Eventuali datagrammi accodati per la ricezione vengono eliminati se il nuovo indirizzo è diverso dall'indirizzo specificato in **un precedente WSPConnect**.

Se l'indirizzo fornito per il socket è tutto zero, il socket verrà disconnesso. L'indirizzo remoto predefinito sarà indeterminato, quindi le chiamate [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) restituiranno il codice di errore WSAENOTCONN, anche se È comunque possibile usare [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e [**WSPRecvFrom.**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))

 

 
