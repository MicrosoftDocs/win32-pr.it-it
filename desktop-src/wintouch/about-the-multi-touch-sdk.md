---
title: Informazioni Windows Touch
description: Questo argomento offre una breve panoramica di Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, software development kit
- Windows Tocco, SDK
- Windows Tocco, informazioni
- Windows Tocco, nuove funzionalità
- Windows Tocco, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3d86270ea6c43cc37c39a5d29282a0451dd38d312b996041dcd21f30de8d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881532"
---
# <a name="about-windows-touch"></a>Informazioni Windows Touch

Questo argomento offre una breve panoramica di Windows Touch.

I nuovi elementi hardware e API nel sistema operativo Windows 7 offrono alle applicazioni la possibilità di ricevere input da più contatti. In questo modo tali applicazioni possono rilevare e rispondere a più punti di tocco simultanei sulla superficie visibile dell'applicazione. La funzionalità per questa funzionalità in Windows 7 è fornita da un nuovo messaggio che segnala e tiene traccia dei tocchi. Il nuovo [**messaggio, WM \_ TOUCH,**](wm-touchdown.md)segnala l'azione (su, giù, spostamento), la posizione e un identificatore per i punti di tocco. Windows I messaggi di tocco vengono generati da Windows e vengono recapitati alle finestre che si registrano per l Windows'input tocco.

Oltre al nuovo messaggio di input tocco, i messaggi di movimento sono stati aggiunti all'elenco esistente di messaggi della finestra. Il supporto della messaggistica per i movimenti è abilitato da un singolo nuovo messaggio della finestra [**(WM \_ GESTURE)**](wm-gesture.md)che viene inviato o inviato alle finestre dell'applicazione appropriate quando l'input dell'utente viene riconosciuto come movimento. Le funzioni API dedicate incapsulano i dettagli per la creazione e l'utilizzo di questo messaggio. Questa operazione viene eseguita perché le informazioni associate al messaggio possono cambiare in futuro senza interrompere le applicazioni che utilizzano già questo messaggio.

Oltre ai messaggi di movimento, sono state aggiunte interfacce specializzate a Windows SDK. Queste interfacce abilitano il supporto avanzato per l'input tocco in modo che gli sviluppatori di applicazioni possano creare facilmente interfacce utente naturali. [**L'interfaccia IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta i messaggi [**WM \_ TOUCH**](wm-touchdown.md) per generare eventi che contengono informazioni su traslazione, rotazione e scala su una raccolta di punti di tocco. [**L'interfaccia IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) può essere usata insieme all'interfaccia **IManipulationProcessor** per abilitare l'animazione e garantire che gli oggetti rimangano sullo schermo dell'utente quando vengono spostati.

Gli elementi API per Windows Touch hanno alcune analogie con Microsoft PixelSense SDK (precedentemente noto come Microsoft Surface SDK), ma le applicazioni che hanno come destinazione Microsoft PixelSense non vengono eseguite nei computer Windows Touch. Inoltre, le applicazioni Windows Touch non vengono eseguite in Microsoft PixelSense.

Alcune delle funzionalità di Windows Touch sono integrate nella base di Windows 7. Questa funzionalità è disponibile per gli utenti senza la necessità per gli sviluppatori di abilitare in modo esplicito il supporto. Tuttavia, per sfruttare al meglio Windows Touch, gli sviluppatori devono usare l'API Windows Touch. Per iniziare a imparare a usare Windows Touch, vedere la Guida alla programmazione o iniziare con Scelta dell'approccio più Windows [Touch.](choosing-the-right-approach-to-windows-touch.md) [](programming-guide.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'architettura](architectural-overview.md)
</dt> <dt>

[Scelta dell'approccio più Windows touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows tocco](windows-touch-portal.md)
</dt> </dl>

 

 




