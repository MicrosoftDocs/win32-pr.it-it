---
title: Informazioni sulla sincronizzazione dei dispositivi
description: Informazioni sulla sincronizzazione dei dispositivi
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Windows Media Player a oggetti, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Windows Media Player ActiveX, sincronizzazione dei dispositivi
- ActiveX, sincronizzazione dei dispositivi
- Windows Media Player controllo ActiveX dispositivi mobili, sincronizzazione dei dispositivi
- Windows Media Player dispositivi mobili, sincronizzazione dei dispositivi
- sincronizzazione di dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione di dispositivi, trasferimento manuale
- sincronizzazione dei dispositivi, trasferimento manuale
- sincronizzazione di dispositivi, sincronizzazione automatica
- sincronizzazione dei dispositivi, sincronizzazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6a03781121a58bee36fd9ff1f74bf21a85347f81384f30c2db5afb4ef3e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903561"
---
# <a name="about-device-synchronization"></a>Informazioni sulla sincronizzazione dei dispositivi

Windows Media Player 10 ha introdotto un nuovo modello per la sincronizzazione del contenuto multimediale digitale con dispositivi portatili. Dal punto di vista dell'utente, ciò significa che è possibile specificare quali playlist (incluse le playlist auto) si sincronizzano automaticamente con i dispositivi. È anche possibile trasferire manualmente il contenuto multimediale digitale ai dispositivi. Dal punto di vista dello sviluppatore, ciò significa che sono esposte nuove funzionalità che è possibile sfruttare nelle applicazioni. A tale scopo, è necessario creare un'istanza remota del controllo Windows Media Player remoto.

Un utente può copiare contenuto multimediale digitale in un dispositivo in due modi:

-   **Trasferimento manuale.** L'utente seleziona il contenuto multimediale digitale nella raccolta e quindi avvia un trasferimento del contenuto al dispositivo. È simile alla funzionalità fornita dalle versioni precedenti di Windows Media Player. L Windows Media Player SDK non fornisce metodi per il trasferimento di file multimediali digitali a un dispositivo.
-   **Sincronizzazione automatica.** L'utente specifica le playlist che si sincronizzano automaticamente con il dispositivo. Si tratta di una funzionalità di Windows Media Player 10 o versioni successive. L'SDK Windows Media Player offre funzionalità per la gestione della sincronizzazione automatica. Questa funzionalità è progettata per consentire di compilare un'interfaccia utente personalizzata per l'applicazione per specificare come avviene la sincronizzazione dei dispositivi e per fornire informazioni sullo stato agli utenti.

Per il funzionamento della sincronizzazione automatica, deve essere stabilita una relazione speciale tra Windows Media Player e il dispositivo. Questa relazione è denominata *relazione*.

Le sezioni seguenti forniscono altre informazioni sulla sincronizzazione dei dispositivi.

-   [Informazioni sui dispositivi](about-devices.md)
-   [Informazioni sulle partnership](about-partnerships.md)
-   [Informazioni sul motore di sincronizzazione](about-the-synchronization-engine.md)
-   [Informazioni sulla sincronizzazione delle playlist](about-playlist-synchronization.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




