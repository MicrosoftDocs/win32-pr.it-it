---
description: Le funzioni seguenti vengono usate con le risorse di comunicazione.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Funzioni di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f49efccf2ff93ea18710ea4d6647e45f1135cf8a5fed542a65192f0abda6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768961"
---
# <a name="communications-functions"></a>Funzioni di comunicazione

Le funzioni seguenti vengono usate con le risorse di comunicazione.



| Funzione                                                   | Descrizione                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Riempie una struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) specificata con i valori specificati in una stringa di controllo del dispositivo.                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Converte una stringa di definizione del dispositivo in codici di blocco di controllo del dispositivo appropriati e li inserisce in un blocco di controllo del dispositivo. |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Ripristina la trasmissione di caratteri per un dispositivo di comunicazione specificato e inserisce la riga di trasmissione in uno stato non di interruzione.    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Recupera informazioni su un errore di comunicazione e segnala lo stato corrente di un dispositivo di comunicazione.                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Visualizza una finestra di dialogo di configurazione fornita dal driver.                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Indica a un dispositivo di comunicazione specificato di eseguire una funzione estesa.                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Recupera la configurazione corrente di un dispositivo di comunicazione.                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Recupera il valore della maschera di evento per un dispositivo di comunicazione specificato.                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Recupera i valori del registro di controllo del modem.                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Recupera informazioni sulle proprietà delle comunicazioni per un dispositivo di comunicazione specificato.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Recupera le impostazioni di controllo correnti per un dispositivo di comunicazione specificato.                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Recupera i parametri di timeout per tutte le operazioni di lettura e scrittura in un dispositivo di comunicazione specificato.                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Recupera la configurazione predefinita per il dispositivo di comunicazione specificato.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Rimuove tutti i caratteri dal buffer di output o di input di una risorsa di comunicazione specificata.                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Sospende la trasmissione di caratteri per un dispositivo di comunicazione specificato e inserisce la riga di trasmissione in uno stato di interruzione.       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Imposta la configurazione corrente di un dispositivo di comunicazione.                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Specifica un set di eventi da monitorare per un dispositivo di comunicazione.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Configura un dispositivo di comunicazione in base alle specifiche in un blocco di controllo del dispositivo.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Imposta i parametri di timeout per tutte le operazioni di lettura e scrittura in un dispositivo di comunicazione specificato.                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Imposta la configurazione predefinita per un dispositivo di comunicazione.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Inizializza i parametri di comunicazione per un dispositivo di comunicazione specificato.                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Trasmette un carattere specificato prima di tutti i dati in sospeso nel buffer di output del dispositivo di comunicazione specificato.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Attende che si verifichi un evento per un dispositivo di comunicazione specificato.                                                             |



 

 

 



