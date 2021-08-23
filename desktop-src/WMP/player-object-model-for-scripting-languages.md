---
title: Modello a oggetti lettore per linguaggi di scripting
description: Modello a oggetti lettore per linguaggi di scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player,modello a oggetti
- Windows Media Player a oggetti, informazioni
- modello a oggetti, informazioni
- Windows Media Player ActiveX, modello a oggetti
- ActiveX, modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- software development kit (SDK), Windows Media Player ActiveX a oggetti di controllo
- SDK (Software Development Kit), Windows Media Player ActiveX a oggetti di controllo
- documentazione, modello Windows Media Player ActiveX a oggetti di controllo
- Windows Media Player,linguaggi di scripting
- Windows Media Player a oggetti, linguaggi di scripting
- modello a oggetti, linguaggi di scripting
- Windows Media Player ActiveX, linguaggi di scripting
- ActiveX, linguaggi di scripting
- Windows Media Player Controllo ActiveX per dispositivi mobili, linguaggi di scripting
- Windows Media Player Dispositivi mobili, linguaggi di scripting
- linguaggi di scripting
- Windows Media Player,Oggetto Player
- Windows Media Player a oggetti, oggetto Player
- modello a oggetti,oggetto Player
- Windows Media Player ActiveX, oggetto Player
- ActiveX, oggetto Player
- Windows Media Player Controllo ActiveX mobile, oggetto Player
- Windows Media Player Mobile, oggetto Player
- Oggetto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996027"
---
# <a name="player-object-model-for-scripting-languages"></a>Modello a oggetti lettore per linguaggi di scripting

ActiveX usa il concetto di oggetti per contenere funzionalità di programmazione. Windows Media Player diversi oggetti per dividere le funzionalità fornite dal controllo. L'oggetto radice è **l'oggetto Player** e gli altri oggetti vengono associati all'oggetto **Player** tramite proprietà specifiche.

Il diagramma seguente illustra il funzionamento del modello Windows Media Player 11 ActiveX a oggetti di controllo per i linguaggi di scripting.

![Diagramma del modello a oggetti di Windows Media Player 11](images/playeromdiag.png)

In C++ e talvolta nei linguaggi .NET gli oggetti sono rappresentati da interfacce COM. Nel modello Windows Media Player a oggetti, i nomi delle interfacce COM sono uguali al nome dell'oggetto, ma hanno il prefisso "IWMP". Ad esempio, **l'oggetto Network** viene esposto tramite **l'interfaccia IWMPNetwork.**

Le sezioni seguenti forniscono panoramiche concettuali per ogni oggetto:

-   [Informazioni sugli oggetti Cdrom e CdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Informazioni sull'oggetto ClosedCaption](about-the-closedcaption-object.md)
-   [Informazioni sull'oggetto Controls](about-the-controls-object.md)
-   [Informazioni sull'oggetto DVD](about-the-dvd-object.md)
-   [Informazioni sugli oggetti Error e ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Informazioni sugli oggetti MediaCollection e Media Objects](about-the-mediacollection-and-media-objects.md)
-   [Informazioni sull'oggetto MetadataPicture](about-the-metadatapicture-object.md)
-   [Informazioni sull'oggetto MetadataText](about-the-metadatatext-object.md)
-   [Informazioni sull'oggetto di rete](about-the-network-object.md)
-   [Informazioni sull'oggetto Lettore](about-the-player-object.md)
-   [Informazioni sull'oggetto PlayerApplication](about-the-playerapplication-object.md)
-   [Informazioni sugli oggetti Playlist, PlaylistCollection e PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Informazioni sull'oggetto Query](about-the-query-object.md)
-   [Informazioni sull'oggetto Impostazioni](about-the-settings-object.md)
-   [Informazioni sull'oggetto StringCollection](about-the-stringcollection-object.md)

Funzionalità aggiuntive sono disponibili tramite determinate interfacce COM. L'accesso a queste interfacce può dipendere dal linguaggio usato per la programmazione e da altri fattori, ad esempio la modalità usata per creare l'istanza del Windows Media Player controllo. Per un elenco completo delle interfacce COM esposte dal controllo Windows Media Player, vedere Object Model Reference for C++ (Informazioni di riferimento sul modello a oggetti [per C++).](object-model-reference-for-c.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Uso del controllo Windows Media Player in una .NET Framework soluzione**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




