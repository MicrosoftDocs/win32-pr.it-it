---
description: Ruoli del dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Ruoli del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386a3ba163a9a82d01aa7916139edaa01e531160f5245c6e751fb7169702de5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018435"
---
# <a name="device-roles"></a>Ruoli del dispositivo

Se un sistema contiene due o più dispositivi endpoint di rendering audio, un dispositivo potrebbe essere ideale per la riproduzione di un tipo di contenuto audio e un altro dispositivo potrebbe essere ideale per la riproduzione di un altro tipo di contenuto. Ad esempio, se un sistema ha due dispositivi di rendering, l'utente può scegliere di riprodurre musica in un dispositivo e di riprodurre i suoni di notifica di sistema sull'altro.

Analogamente, se un sistema contiene due o più dispositivi endpoint di acquisizione audio, un dispositivo potrebbe essere ideale per l'acquisizione di un tipo di contenuto audio e un altro dispositivo potrebbe essere ideale per l'acquisizione di un altro tipo di contenuto. Ad esempio, se un sistema ha due dispositivi di acquisizione, l'utente potrebbe scegliere di registrare musica live in un dispositivo e di usare l'altro dispositivo per i comandi vocali.

I dispositivi possono avere tre ruoli: Console, Comunicazioni e Multimedia. La tabella seguente descrive i ruoli dei dispositivi identificati dalle tre costanti, eConsole, eCommunications e eMultimedia, [**nell'enumerazione ERole.**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)



| Costante ERole  | Ruolo del dispositivo                              | Esempi di rendering             | Esempi di acquisizione                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interazione con il computer            | Giochi e notifiche di sistema | Comandi vocali                     |
| eCommunications | Comunicazioni vocali con un'altra persona | Chat e VoIP                  | Chat e VoIP                      |
| eMultimedia     | Riproduzione o registrazione di contenuto audio       | Musica e film               | Narrazione e registrazione di musica live |



 

A un particolare dispositivo di rendering o acquisizione potrebbe essere assegnato nessuno, uno, alcuni o tutti i ruoli nella tabella precedente. In qualsiasi momento, ogni ruolo nella tabella viene assegnato a un dispositivo di rendering (e a un solo) dispositivo di acquisizione. Ciò significa che l'assegnazione dei ruoli ai dispositivi di rendering è indipendente dall'assegnazione dei ruoli per acquisire i dispositivi.

Un'applicazione potrebbe scegliere di riprodurre tutti i flussi di output tramite un singolo dispositivo endpoint di rendering e di registrare tutti i flussi di input da un singolo dispositivo endpoint di acquisizione. In alternativa, un'applicazione potrebbe scegliere di riprodurre alcuni dei flussi di output tramite un dispositivo di rendering e di riprodurre altri flussi di output tramite un altro dispositivo di rendering. Analogamente, potrebbe scegliere di registrare alcuni dei flussi di input tramite un dispositivo di acquisizione e di registrare altri flussi di input tramite un altro dispositivo di acquisizione. In tutti i casi, l'applicazione può assegnare ogni flusso al dispositivo il cui ruolo è più appropriato per tale flusso.

Ad esempio, un'applicazione VoIP potrebbe assegnare il flusso di output che contiene la notifica dell'anello al dispositivo endpoint di rendering con il ruolo eConsole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> <dt>

[Uso dei ruoli del dispositivo](device-roles-in-windows-vista.md)
</dt> <dt>

[Interoperabilità con LE API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



