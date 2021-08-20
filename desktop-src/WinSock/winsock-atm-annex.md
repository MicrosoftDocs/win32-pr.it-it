---
description: AtM è applicabile sia agli ambienti LAN che WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM Annex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f55c71b830fa8a5f27f083af0263c62766e7b037e433c04b73bfea5ba12960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822447"
---
# <a name="winsock-atm-annex"></a>Winsock ATM Annex

AtM è applicabile sia agli ambienti LAN che WAN. Una rete ATM trasporta contemporaneamente un'ampia gamma di traffico di rete, ad esempio voce, dati, immagini e video. Offre agli utenti una qualità del servizio garantita in base al canale virtuale .



| Elemento          | Descrizione                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i protocollo/i | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Descrizione      | ATM AAL5 offre un servizio di trasporto orientato alla connessione, con limiti di messaggi mantenuti e garantiti da QOS. ATMPROTO \_ AALUSER è un AAL definito dall'utente. |
| Famiglia di indirizzi   | BANCOMAT DI AF \_                                                                                                                                                     |
| File di intestazione      | Ws2atm.h                                                                                                                                                    |



 

Questa sezione descrive le estensioni specifiche della modalità di trasferimento asincrono (ATM) necessarie per supportare i servizi ATM nativi esposti e specificati nella specifica UNI (User Network Interface) del forum ATM versione 3.x (3.0 e 3.1). Questo documento supporta AAL di tipo 5 (modalità messaggio) e AAL definito dall'utente. Le versioni future di questo documento supporteranno altri tipi di AAL e UNI 4.0.

 

 



