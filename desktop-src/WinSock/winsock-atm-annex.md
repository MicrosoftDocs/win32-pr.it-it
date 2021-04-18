---
description: ATM è applicabile agli ambienti LAN e WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Allegato ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308864"
---
# <a name="winsock-atm-annex"></a>Allegato ATM Winsock

ATM è applicabile agli ambienti LAN e WAN. Una rete ATM trasporta simultaneamente un'ampia gamma di traffico di rete: voce, dati, immagine e video. Fornisce agli utenti una qualità del servizio garantita in base a un canale virtuale (VC).



| Elemento          | Descrizione                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i protocollo | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Descrizione      | AAL5 ATM fornisce un servizio di trasporto che è orientato alla connessione, mantenuto al limite dei messaggi e garantito QOS. ATMPROTO \_ AALUSER è un Aal definito dall'utente. |
| Famiglia di indirizzi   | \_ATM AF                                                                                                                                                     |
| File di intestazione      | Ws2atm. h                                                                                                                                                    |



 

In questa sezione vengono descritte le estensioni specifiche di ATM (Asynchronous Transfer Mode) necessarie per supportare i servizi ATM nativi come esposti e specificati nella specifica della versione 3. x (3,0 e 3,1) di ATM Forum User Network Interface (UNI). Questo documento supporta AAL di tipo 5 (modalità messaggio) e AAL definito dall'utente. Le versioni future di questo documento supporteranno altri tipi di AAL, nonché UNI 4,0.

 

 



