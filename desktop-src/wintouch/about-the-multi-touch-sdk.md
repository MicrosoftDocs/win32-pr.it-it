---
title: Informazioni su Windows Touch
description: Questo argomento fornisce una breve panoramica di Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, Software Development Kit
- Windows Touch, SDK
- Windows Touch, informazioni
- Windows Touch, nuove funzionalità
- Windows Touch, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955190"
---
# <a name="about-windows-touch"></a>Informazioni su Windows Touch

Questo argomento fornisce una breve panoramica di Windows Touch.

I nuovi elementi hardware e API del sistema operativo Windows 7 consentono alle applicazioni di ricevere input da più contatti. Questo consente alle applicazioni di rilevare e rispondere a più punti di tocco simultanei sulla superficie visibile dell'applicazione. La funzionalità per questa funzionalità di Windows 7 è fornita da un nuovo messaggio che segnala e tiene traccia dei ritocchi. Il nuovo messaggio, [**WM \_ touch**](wm-touchdown.md), segnala l'azione (verso l'alto, verso il basso, lo spostamento), la posizione e un identificatore per i punti di tocco. I messaggi Windows Touch vengono generati da Windows e vengono recapitati a Windows registrati per l'input di Windows Touch.

Oltre al nuovo messaggio di input tocco, i messaggi di movimento sono stati aggiunti all'elenco esistente di messaggi di finestra. Il supporto della messaggistica per i movimenti è abilitato da un singolo messaggio di finestra ([**\_ gesto WM**](wm-gesture.md)) che viene inviato o inviato alle finestre dell'applicazione appropriate quando l'input dell'utente viene riconosciuto come un movimento. Le funzioni API dedicate incapsulano i dettagli per la creazione e l'utilizzo di questo messaggio. Questa operazione viene eseguita perché le informazioni associate al messaggio possono cambiare in futuro senza compromettere le applicazioni che già utilizzano questo messaggio.

Oltre ai messaggi di movimento, le interfacce specializzate sono state aggiunte al Windows SDK. Queste interfacce consentono un supporto avanzato per l'input tocco, in modo che gli sviluppatori di applicazioni possano creare facilmente interfacce utente naturali. L'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta i messaggi [**WM \_ touch**](wm-touchdown.md) per generare eventi che contengono informazioni sulla conversione, la rotazione e la scalabilità di una raccolta di punti di tocco. L'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) può essere usata insieme all'interfaccia **IManipulationProcessor** per abilitare l'animazione e verificare che gli oggetti restino sullo schermo dell'utente quando vengono spostati.

Gli elementi API per Windows Touch hanno alcune somiglianze con Microsoft PixelSense SDK (noto in precedenza come Microsoft Surface SDK), ma le applicazioni destinate a Microsoft PixelSense non vengono eseguite nei computer Windows Touch. Inoltre, le applicazioni destinate a Windows Touch non vengono eseguite su Microsoft PixelSense.

Alcune delle funzionalità di Windows Touch sono incorporate nel nucleo di Windows 7. Questa funzionalità è disponibile per gli utenti senza la necessità per gli sviluppatori di abilitare in modo esplicito il supporto. Tuttavia, per sfruttare al meglio Windows Touch, gli sviluppatori devono utilizzare l'API Windows Touch. Per iniziare a conoscere il funzionamento di Windows Touch, vedere la [Guida alla programmazione](programming-guide.md) o iniziare a [scegliere l'approccio più appropriato per Windows Touch](choosing-the-right-approach-to-windows-touch.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'architettura](architectural-overview.md)
</dt> <dt>

[Scelta dell'approccio giusto per Windows Touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Touch](windows-touch-portal.md)
</dt> </dl>

 

 




