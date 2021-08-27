---
title: Documento ServiceInfo
description: Documento ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player negozi online, documento ServiceInfo
- negozi online, documento ServiceInfo
- tipo 1 negozi online, documento ServiceInfo
- Tipo 2 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88863bb75cd0a7b85bead1c20759b77710c2db483b4d9e48ed1f53741dd0840d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995421"
---
# <a name="serviceinfo-document"></a>Documento ServiceInfo

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

I negozi online devono creare il ServiceInfo.xml documento. Si tratta del documento utilizzato dal negozio online per configurare l'interfaccia utente Windows Media Player quando Windows Media Player 10 o versione successiva ospita il negozio online.

Gli elementi seguenti e i relativi attributi sono supportati per i Windows Media Player online.



| Elemento                                      | Descrizione                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Specifica l'URL della pagina Web Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale. Tipo 1: facoltativo<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: ignorato<br/>                                |
| [ButtonText](buttontext-element.md)         | Specifica la stringa di testo visualizzata Windows Media Player per un pulsante del riquadro attività. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                             |
| [Descrizione comando](buttontip-element.md)           | Specifica la descrizione comando visualizzata quando l'utente punta a un pulsante del riquadro attività. Tipo 1: facoltativo<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Specifica gli URL per le pagine Web Windows Media Player quando l'utente sceglie di effettuare un acquisto. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: ignorato<br/>                                                                      |
| [Colore](color-element.md)                   | Specifica il colore di sfondo per i pulsanti di spostamento dei negozi online. Tipo 1: facoltativo<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                             |
| [Descrizione](description-element.md)       | Specifica una descrizione del negozio online che viene visualizzata durante la prima esperienza dell'utente con un'installazione di Windows Media Player. Richiede Windows Media Player 11.Type 1: obbligatorio<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/> |
| [DownloadStatus](downloadstatus-element.md) | Specifica un URL visualizzato dal Windows Media Player come collegamento per consentire agli utenti di visualizzare lo stato di download. Tipo 1: ignorato<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Specifica la stringa di testo Windows Media Player all'utente per identificare il negozio online. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Specifica l'URL di base di una pagina Web HTMLView. Tipo 1: facoltativo<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                   |
| [Immagine](image-element.md)                   | Specifica le immagini che Windows Media Player all'utente per rappresentare il negozio online. Tipo 1: obbligatorio<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                               |
| [Infocenter](infocenter-element.md)         | Specifica l'URL della pagina Web Windows Media Player visualizzata nella funzionalità Visualizzazione Info Center di In riproduzione **quando** il negozio online è attivo. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: ignorato<br/>                           |
| [Installazione](install-element.md)               | Specifica i valori usati dal Windows Media Player per installare il negozio online predefinito. Tipo 1: obbligatorio<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: ignorato<br/>                                                                                          |
| [Navigare](navigate-element.md)             | Specifica un URL di base utilizzato dalle chiamate a **External.NavigateTaskPaneURL**. Tipo 1: facoltativo<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Rappresenta l'elemento main per il ServiceInfo.xml documento. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Rappresenta il primo riquadro attività del negozio online. Tipo 1: obbligatorio<br/> Tipo 2 Musica: obbligatorio<br/> Tipo 2 Commerce: obbligatorio<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Rappresenta il secondo riquadro attività del negozio online. Tipo 1: ignorato<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Rappresenta il terzo riquadro attività del negozio online. Tipo 1: ignorato<br/> Tipo 2 Musica: facoltativo<br/> Tipo 2 Commerce: facoltativo<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





