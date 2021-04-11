---
title: Documento ServiceInfo
description: Documento ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044363"
---
# <a name="serviceinfo-document"></a>Documento ServiceInfo

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Gli archivi online devono creare il documento ServiceInfo.xml. Si tratta del documento utilizzato dall'archivio online per configurare l'interfaccia utente di Windows Media Player quando Windows Media Player 10 o versione successiva ospita lo Store online.

Gli elementi e i relativi attributi seguenti sono supportati per gli archivi Windows Media Player online.



| Elemento                                      | Descrizione                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Specifica l'URL per la pagina Web visualizzata da Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale. Tipo 1: facoltativo<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: ignorato<br/>                                |
| [ButtonText](buttontext-element.md)         | Specifica la stringa di testo visualizzata da Windows Media Player per un pulsante del riquadro attività. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Specifica la descrizione comando visualizzata quando l'utente punta a un pulsante del riquadro attività. Tipo 1: facoltativo<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Specifica gli URL per le pagine Web visualizzate da Windows Media Player quando l'utente sceglie di effettuare un acquisto. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: ignorato<br/>                                                                      |
| [Colore](color-element.md)                   | Specifica il colore di sfondo per i pulsanti di spostamento dei negozi online. Tipo 1: facoltativo<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                             |
| [Descrizione](description-element.md)       | Specifica una descrizione dell'archivio online visualizzato durante la prima esperienza dell'utente con un'installazione di Windows Media Player. Richiede Windows Media Player 11. tipo 1: obbligatorio<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/> |
| [DownloadStatus](downloadstatus-element.md) | Specifica un URL visualizzato da Windows Media Player come collegamento per consentire agli utenti di visualizzare lo stato del download. Tipo 1: ignorato<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Specifica la stringa di testo che Windows Media Player visualizza all'utente per identificare il negozio online. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Specifica l'URL di base di una pagina Web HTMLView. Tipo 1: facoltativo<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                   |
| [Immagine](image-element.md)                   | Specifica le immagini che Windows Media Player visualizza all'utente per rappresentare l'archivio online. Tipo 1: obbligatorio<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                               |
| [Centro informazioni per](infocenter-element.md)         | Specifica l'URL della pagina Web visualizzata da Windows Media Player nella funzionalità di visualizzazione del centro informazioni in cui viene **ora riprodotto** quando lo Store online è attivo. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: ignorato<br/>                           |
| [Installazione](install-element.md)               | Specifica i valori utilizzati dal programma di installazione di Windows Media Player per installare l'archivio online predefinito. Tipo 1: obbligatorio<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: ignorato<br/>                                                                                          |
| [Navigare](navigate-element.md)             | Specifica un URL di base usato dalle chiamate a **External. NavigateTaskPaneURL**. Tipo 1: facoltativo<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Rappresenta l'elemento principale per il documento ServiceInfo.xml. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Rappresenta il primo riquadro attività negozio online. Tipo 1: obbligatorio<br/> Tipo 2 musica: obbligatoria<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Rappresenta il secondo riquadro attività archivio online. Tipo 1: ignorato<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Rappresenta il terzo riquadro attività negozio online. Tipo 1: ignorato<br/> Tipo 2 musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





