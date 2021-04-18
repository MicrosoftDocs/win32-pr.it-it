---
title: Informazioni sulla sincronizzazione dei dispositivi
description: Informazioni sulla sincronizzazione dei dispositivi
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Modello a oggetti di Windows Media Player, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Controllo ActiveX di Windows Media Player, sincronizzazione dei dispositivi
- Controllo ActiveX, sincronizzazione dei dispositivi
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione dei dispositivi
- Windows Media Player Mobile, sincronizzazione dei dispositivi
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, trasferimento manuale
- sincronizzazione dei dispositivi, trasferimento manuale
- sincronizzazione dei dispositivi, sincronizzazione automatica
- sincronizzazione dei dispositivi, sincronizzazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298115"
---
# <a name="about-device-synchronization"></a>Informazioni sulla sincronizzazione dei dispositivi

Windows Media Player 10 ha introdotto un nuovo modello per sincronizzare il contenuto multimediale digitale con i dispositivi portatili. Dal punto di vista dell'utente, ciò significa che è possibile specificare le playlist (incluse le playlist automatiche) sincronizzate automaticamente con i dispositivi. È anche possibile trasferire manualmente il contenuto multimediale digitale ai dispositivi. Dal punto di vista dello sviluppatore, ciò significa che sono presenti nuove funzionalità esposte che è possibile utilizzare nelle applicazioni. A tale scopo, è necessario creare un'istanza remota del controllo Media Player di Windows.

Esistono due modi in cui un utente può copiare il contenuto multimediale digitale in un dispositivo:

-   **Trasferimento manuale.** L'utente seleziona il contenuto multimediale digitale nella libreria e quindi avvia il trasferimento del contenuto al dispositivo. Questa funzionalità è simile a quella fornita dalle versioni precedenti di Windows Media Player. Windows Media Player SDK non fornisce metodi per il trasferimento di file multimediali digitali a un dispositivo.
-   **Sincronizzazione automatica.** L'utente specifica le playlist che vengono sincronizzate automaticamente con il dispositivo. Si tratta di una funzionalità di Windows Media Player 10 o versione successiva. Windows Media Player SDK fornisce funzionalità per la gestione della sincronizzazione automatica. Questa funzionalità è progettata per consentire di creare un'interfaccia utente personalizzata per l'applicazione per specificare la modalità di sincronizzazione dei dispositivi e per fornire informazioni sullo stato agli utenti.

Per il corretto funzionamento della sincronizzazione automatica, è necessario stabilire una relazione speciale tra Windows Media Player e il dispositivo. Questa relazione è detta *collaborazione*.

Le sezioni seguenti forniscono altre informazioni sulla sincronizzazione dei dispositivi.

-   [Informazioni sui dispositivi](about-devices.md)
-   [Informazioni sulle relazioni](about-partnerships.md)
-   [Informazioni sul motore di sincronizzazione](about-the-synchronization-engine.md)
-   [Informazioni sulla sincronizzazione della playlist](about-playlist-synchronization.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Uso dei dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




