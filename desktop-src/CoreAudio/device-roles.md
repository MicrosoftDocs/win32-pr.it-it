---
description: Ruoli del dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Ruoli del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126902"
---
# <a name="device-roles"></a>Ruoli del dispositivo

Se un sistema contiene due o più dispositivi endpoint per il rendering audio, un dispositivo potrebbe essere più adatto per la riproduzione di un tipo di contenuto audio e un altro dispositivo potrebbe essere migliore per la riproduzione di un altro tipo di contenuto. Ad esempio, se un sistema dispone di due dispositivi di rendering, l'utente potrebbe scegliere di riprodurre musica in un dispositivo e di riprodurre suoni di notifica di sistema sull'altro.

Analogamente, se un sistema contiene due o più dispositivi endpoint di acquisizione audio, un dispositivo potrebbe essere più adatto per l'acquisizione di un tipo di contenuto audio e un altro dispositivo potrebbe essere migliore per l'acquisizione di un altro tipo di contenuto. Ad esempio, se un sistema dispone di due dispositivi di acquisizione, l'utente può scegliere di registrare musica in tempo reale in un dispositivo e di usare l'altro dispositivo per i comandi vocali.

I dispositivi possono avere tre ruoli: console, comunicazioni e multimedia. nella tabella seguente vengono descritti i ruoli del dispositivo identificati dalle tre costanti, ovvero eConsole, comunicazioni elettroniche e eMultimedia, nell'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .



| Costante ERole  | Ruolo del dispositivo                              | Esempi di rendering             | Esempi di acquisizione                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interazione con il computer            | Giochi e notifiche di sistema | Comandi vocali                     |
| Comunicazioni elettroniche | Comunicazioni vocali con un'altra persona | Chat e VoIP                  | Chat e VoIP                      |
| eMultimedia     | Riproduzione o registrazione di contenuto audio       | Musica e film               | Registrazione e musica in diretta |



 

A un particolare dispositivo di rendering o acquisizione potrebbe essere assegnato nessuno, uno, alcuni o tutti i ruoli nella tabella precedente. Ogni ruolo della tabella viene assegnato in qualsiasi momento a uno (e un solo) dispositivo di rendering e a un solo dispositivo di acquisizione. Ovvero, l'assegnazione dei ruoli ai dispositivi di rendering è indipendente dall'assegnazione dei ruoli per l'acquisizione di dispositivi.

Un'applicazione può scegliere di riprodurre tutti i flussi di output tramite un singolo dispositivo endpoint di rendering e di registrare tutti i flussi di input da un singolo dispositivo dell'endpoint di acquisizione. In alternativa, un'applicazione può scegliere di riprodurre alcuni flussi di output tramite un dispositivo di rendering e di riprodurre altri flussi di output tramite un altro dispositivo di rendering. Analogamente, può scegliere di registrare alcuni dei flussi di input attraverso un dispositivo di acquisizione e di registrare altri flussi di input tramite un altro dispositivo di acquisizione. In tutti i casi, l'applicazione può assegnare ogni flusso al dispositivo il cui ruolo è più appropriato per il flusso.

Ad esempio, un'applicazione VoIP potrebbe assegnare il flusso di output che contiene la notifica circolare al dispositivo dell'endpoint di rendering con il ruolo eConsole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[Utilizzo dei ruoli del dispositivo](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



