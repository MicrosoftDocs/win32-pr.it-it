---
description: "Windows Le funzioni e i metodi di acquisizione delle immagini (WIA) possono restituire codici di errore dall'elenco seguente: Codice di erroreCodiceCODICEWIA ERRORE OCCUPATOIl dispositivo \\_ \\_ è occupato."
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Codici di errore (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c782ae449a52ae0ff2b64f124609a3142f1dd457d74bdb82333502ef1868ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670274"
---
# <a name="error-codes-wia"></a>Codici di errore (WIA)

Windows Le funzioni e i metodi di acquisizione di immagini (WIA) possono restituire codici di errore dall'elenco seguente: 

| Codice di errore                                      | Significato                                                                                                                                                                                                                             | Codice       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| ERRORE WIA \_ \_ OCCUPATO                                | Il dispositivo è occupato. Chiudere tutte le app che usano questo dispositivo o attendere il completamento, quindi riprovare.                                                                                                                          | 0x80210006 |
| WIA \_ ERROR \_ COVER \_ OPEN                         | Una o più cover del dispositivo sono aperte.                                                                                                                                                                                          | 0x80210016 |
| ERRORE WIA \_ COMUNICAZIONE \_ DEL \_ DISPOSITIVO               | La comunicazione con il dispositivo WIA non è riuscita. Assicurarsi che il dispositivo sia acceso e connesso al PC. Se il problema persiste, disconnettere e riconnettere il dispositivo.                                                            | 0x8021000A |
| ERRORE WIA \_ DISPOSITIVO \_ \_ BLOCCATO                      | Il dispositivo è bloccato. Chiudere tutte le app che usano questo dispositivo o attendere il completamento, quindi riprovare.                                                                                                                        | 0x8021000D |
| ECCEZIONE DI ERRORE WIA \_ \_ NEL \_ \_ DRIVER               | Il driver di dispositivo ha generato un'eccezione.                                                                                                                                                                                               | 0x8021000E |
| ERRORE WIA \_ \_ ERRORE \_ GENERALE                      | Si è verificato un errore sconosciuto con il dispositivo WIA.                                                                                                                                                                                  | 0x80210001 |
| ERRORE WIA \_ IMPOSTAZIONE \_ HARDWARE NON \_ \_ CORRETTA        | Nel dispositivo WIA non è presente un'impostazione corretta.                                                                                                                                                                                    | 0x8021000C |
| ERRORE WIA \_ \_ COMANDO NON \_ VALIDO                    | Il dispositivo non supporta questo comando.                                                                                                                                                                                            | 0x8021000B |
| ERRORE WIA \_ RISPOSTA \_ DRIVER NON \_ \_ VALIDA           | La risposta del driver non è valida.                                                                                                                                                                                            | 0x8021000F |
| ELEMENTO DI ERRORE WIA \_ \_ \_ ELIMINATO                       | Il dispositivo WIA è stato eliminato. Non è più disponibile.                                                                                                                                                                               | 0x80210009 |
| WIA \_ ERROR \_ LAMP \_ OFF                           | La lampadina dello scanner è spenta.                                                                                                                                                                                                          | 0x80210017 |
| WIA \_ ERROR \_ MAXIMUM \_ PRINTER \_ ENDORSER \_ COUNTER | Un processo di analisi è stato interrotto perché un elemento Imprinter/Endorser ha raggiunto il valore massimo valido per WIA IPS PRINTER ENDORSER COUNTER ed è stato \_ \_ \_ \_ reimpostato su 0. Questa funzionalità è disponibile con Windows 8 e versioni successive di Windows. | 0x80210021 |
| WIA \_ ERROR \_ MULTI \_ FEED                         | Si è verificato un errore di analisi a causa di una condizione di feed di pagina multipli. Questa funzionalità è disponibile con Windows 8 e versioni successive di Windows.                                                                                            | 0x80210020 |
| ERRORE WIA \_ \_ OFFLINE                             | Il dispositivo è offline. Verificare che il dispositivo sia acceso e connesso al PC.                                                                                                                                                  | 0x80210005 |
| WIA \_ ERROR \_ PAPER \_ EMPTY                        | Non sono presenti documenti nell'alimentatore di documenti.                                                                                                                                                                                      | 0x80210003 |
| WIA \_ ERROR \_ PAPER \_ JAM                          | La carta è inceppata nell'alimentatore di documenti dello scanner.                                                                                                                                                                                   | 0x80210002 |
| PROBLEMA RELATIVO ALLA CARTA \_ DI \_ ERRORE WIA \_                      | Si è verificato un problema non specificato con l'alimentatore di documenti dello scanner.                                                                                                                                                                 | 0x80210004 |
| WIA \_ ERROR \_ WARMING \_ UP                         | Il dispositivo si sta riscaldamento.                                                                                                                                                                                                           | 0x80210007 |
| ERRORE WIA \_ - \_ INTERVENTO \_ DELL'UTENTE                  | Si è verificato un problema con il dispositivo WIA. Assicurarsi che il dispositivo sia acceso, online e che tutti i cavi siano collegati correttamente.                                                                                                      | 0x80210008 |
| WIA S NO DEVICE AVAILABLE (WIA \_ S \_ NESSUN DISPOSITIVO \_ \_ DISPONIBILE)                   | Non è stato trovato alcun dispositivo scanner. Assicurarsi che il dispositivo sia online, connesso al PC e che nel PC sia installato il driver corretto.                                                                                                   | 0x80210015 |



 

 

 



