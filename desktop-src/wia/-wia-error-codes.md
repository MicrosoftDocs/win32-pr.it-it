---
description: "Le funzioni e i metodi di acquisizione immagini Windows (WIA) possono restituire codici di errore dall'elenco seguente: errore CodeMeaningCodeWIA \\_ errore \\_ BUSYThe dispositivo occupato."
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Codici di errore (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6025616d46a5973692bb3cafbcf88e18836ad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879709"
---
# <a name="error-codes-wia"></a>Codici di errore (WIA)

Le funzioni e i metodi Windows Image Acquisition (WIA) possono restituire codici di errore dall'elenco seguente: 

| Codice di errore                                      | Significato                                                                                                                                                                                                                             | Codice       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| \_errore WIA \_ occupato                                | Il dispositivo è occupato. Chiudere le app che usano questo dispositivo o attenderne il completamento, quindi riprovare.                                                                                                                          | 0x80210006 |
| \_coperchio errore \_ WIA \_ aperto                         | Uno o più del coperchio del dispositivo è aperto.                                                                                                                                                                                          | 0x80210016 |
| \_comunicazione del \_ dispositivo con errore WIA \_               | Comunicazione con il dispositivo WIA non riuscita. Verificare che il dispositivo sia acceso e connesso al computer. Se il problema persiste, disconnettere e riconnettere il dispositivo.                                                            | 0x8021000A |
| \_errore WIA \_ dispositivo \_ bloccato                      | Il dispositivo è bloccato. Chiudere le app che usano questo dispositivo o attenderne il completamento, quindi riprovare.                                                                                                                        | 0x8021000D |
| \_ \_ eccezione di errore WIA \_ nel \_ driver               | Il driver di dispositivo ha generato un'eccezione.                                                                                                                                                                                               | 0x8021000E |
| errore \_ generale dell'errore WIA \_ \_                      | Si è verificato un errore sconosciuto con il dispositivo WIA.                                                                                                                                                                                  | 0x80210001 |
| \_errore WIA \_ \_ impostazione hardware non corretta \_        | Impostazione non corretta sul dispositivo WIA.                                                                                                                                                                                    | 0x8021000C |
| \_errore WIA \_ comando non valido \_                    | Il dispositivo non supporta questo comando.                                                                                                                                                                                            | 0x8021000B |
| \_errore WIA \_ \_ risposta driver non valida \_           | Risposta dal driver non valida.                                                                                                                                                                                            | 0x8021000F |
| \_elemento di errore WIA \_ \_ eliminato                       | Il dispositivo WIA è stato eliminato. Non è più disponibile.                                                                                                                                                                               | 0x80210009 |
| \_Lamp di errore WIA \_ \_ disattivato                           | La lampada dello scanner è disattivata.                                                                                                                                                                                                          | 0x80210017 |
| \_errore WIA \_ valore massimo del \_ \_ \_ contatore della stampante | Un processo di analisi è stato interrotto perché un elemento dell'approvatore/approvatore ha raggiunto il valore massimo valido per il \_ \_ contatore della stampante di indirizzi IP WIA \_ \_ ed è stato reimpostato su 0. Questa funzionalità è disponibile con Windows 8 e versioni successive di Windows. | 0x80210021 |
| \_errore WIA \_ - \_ feed più                         | Si è verificato un errore di analisi a causa di una condizione di feed a più pagine. Questa funzionalità è disponibile con Windows 8 e versioni successive di Windows.                                                                                            | 0x80210020 |
| \_errore WIA \_ offline                             | Il dispositivo è offline. Verificare che il dispositivo sia acceso e connesso al computer.                                                                                                                                                  | 0x80210005 |
| \_documento di errore WIA \_ \_ vuoto                        | Non sono presenti documenti nel Feeder del documento.                                                                                                                                                                                      | 0x80210003 |
| \_ \_ Jam paper di errore WIA \_                          | Il materiale cartaceo è bloccato nel feeder di documenti dello scanner.                                                                                                                                                                                   | 0x80210002 |
| \_ \_ problema relativo alla carta di errore WIA \_                      | Si è verificato un problema non specificato con il feeder di documenti dello scanner.                                                                                                                                                                 | 0x80210004 |
| \_errore WIA \_ durante \_ il riscaldamento                         | Il dispositivo è in stato di riscaldamento.                                                                                                                                                                                                           | 0x80210007 |
| \_errore WIA \_ intervento dell'utente \_                  | Si è verificato un problema con il dispositivo WIA. Verificare che il dispositivo sia acceso, online e che i cavi siano connessi correttamente.                                                                                                      | 0x80210008 |
| WIA \_ S \_ nessun \_ dispositivo \_ disponibile                   | Non è stato trovato alcun dispositivo dello scanner. Verificare che il dispositivo sia online, connesso al PC e che nel computer sia installato il driver corretto.                                                                                                   | 0x80210015 |



 

 

 



