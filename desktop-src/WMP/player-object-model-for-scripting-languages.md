---
title: Modello a oggetti del lettore per i linguaggi di scripting
description: Modello a oggetti del lettore per i linguaggi di scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, informazioni
- modello a oggetti, informazioni
- Controllo ActiveX di Windows Media Player, modello a oggetti
- Controllo ActiveX, modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- Software Development Kit (SDK), modello a oggetti del controllo ActiveX di Windows Media Player
- SDK (Software Development Kit), modello a oggetti del controllo ActiveX di Windows Media Player
- documentazione, modello a oggetti del controllo ActiveX di Windows Media Player
- Windows Media Player, linguaggi di scripting
- Modello a oggetti di Windows Media Player, linguaggi di scripting
- modello a oggetti, linguaggi di scripting
- Controllo ActiveX di Windows Media Player, linguaggi di scripting
- Controllo ActiveX, linguaggi di scripting
- Controllo ActiveX Windows Media Player Mobile, linguaggi di scripting
- Windows Media Player Mobile, linguaggi di scripting
- linguaggi di scripting
- Windows Media Player, oggetto Player
- Modello a oggetti di Windows Media Player, oggetto Player
- modello a oggetti, oggetto Player
- Controllo ActiveX Windows Media Player, oggetto Player
- Controllo ActiveX, oggetto Player
- Controllo ActiveX Windows Media Player Mobile, oggetto Player
- Windows Media Player Mobile, oggetto lettore
- Oggetto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551905"
---
# <a name="player-object-model-for-scripting-languages"></a>Modello a oggetti del lettore per i linguaggi di scripting

ActiveX usa il concetto di oggetti per contenere la funzionalità di programmazione. Windows Media Player utilizza diversi oggetti per dividere la funzionalità fornita dal controllo. L'oggetto radice è l'oggetto **Player** e gli altri oggetti sono collegati all'oggetto **Player** tramite proprietà specifiche.

Il diagramma seguente illustra il funzionamento del modello a oggetti del controllo ActiveX di Windows Media Player 11 per i linguaggi di scripting.

![diagramma del modello a oggetti di Windows Media Player 11](images/playeromdiag.png)

In C++, e talvolta nei linguaggi .NET, gli oggetti sono rappresentati da interfacce COM. Nel modello a oggetti di Windows Media Player, i nomi delle interfacce COM corrispondono al nome dell'oggetto, ma sono preceduti da "IWMP". Ad esempio, l'oggetto di **rete** viene esposto tramite l'interfaccia **IWMPNetwork** .

Nelle sezioni seguenti vengono fornite panoramiche concettuali per ogni oggetto:

-   [Informazioni sugli oggetti cdrom e cdromcollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Informazioni sull'oggetto ClosedCaption](about-the-closedcaption-object.md)
-   [Informazioni sull'oggetto Controls](about-the-controls-object.md)
-   [Informazioni sull'oggetto DVD](about-the-dvd-object.md)
-   [Informazioni sugli oggetti Error e ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Informazioni sugli oggetti Mediacollection e media](about-the-mediacollection-and-media-objects.md)
-   [Informazioni sull'oggetto MetadataPicture](about-the-metadatapicture-object.md)
-   [Informazioni sull'oggetto MetadataText](about-the-metadatatext-object.md)
-   [Informazioni sull'oggetto di rete](about-the-network-object.md)
-   [Informazioni sull'oggetto Player](about-the-player-object.md)
-   [Informazioni sull'oggetto PlayerApplication](about-the-playerapplication-object.md)
-   [Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Informazioni sull'oggetto query](about-the-query-object.md)
-   [Informazioni sull'oggetto Settings](about-the-settings-object.md)
-   [Informazioni sull'oggetto StringCollection](about-the-stringcollection-object.md)

Funzionalità aggiuntive sono disponibili tramite determinate interfacce COM. La possibilità di accedere a tali interfacce può dipendere dal linguaggio utilizzato per la programmazione e da altri fattori, ad esempio la modalità utilizzata per creare l'istanza del controllo Media Player di Windows. Per un elenco completo delle interfacce COM esposte dal controllo Media Player Windows, vedere [riferimento del modello a oggetti per C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in una soluzione .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




