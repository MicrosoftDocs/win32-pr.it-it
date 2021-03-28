---
description: Alcuni degli elementi di sistema disponibili nel pannello di controllo sono estendibili. Per installare un'estensione del pannello di controllo, registrare l'estensione della shell nel modo seguente, dove nome è il nome predefinito dell'elemento di sistema (vedere la tabella riportata di seguito).
title: Estensione degli elementi del pannello di controllo di sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993869"
---
# <a name="extending-system-control-panel-items"></a>Estensione degli elementi del pannello di controllo di sistema

Alcuni degli elementi di sistema disponibili nel pannello di controllo sono estendibili. Per installare un'estensione del pannello di controllo, registrare l'estensione della shell nel modo seguente, dove *nome* è il nome predefinito dell'elemento di sistema (vedere la tabella riportata di seguito).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Questa operazione è simile alla modalità di registrazione di un'estensione per un oggetto shell predefinito. Poiché le uniche estensioni della shell supportate dagli elementi del pannello di controllo sono finestre delle proprietà, la registrazione deve trovarsi nella sottochiave **ShellEx** \\ **PropertySheetHandlers**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento del pannello di controllo</th>
<th><em>nome</em></th>
<th>Commenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Visualizza</td>
<td>Reception</td>
<td>Supporta anche la sostituzione della pagina <strong>Desktop</strong> .
<blockquote>
[!Note]<br />
Questa operazione non è più supportata in Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Impostazioni di visualizzazione avanzate</td>
<td>Dispositivo</td>
<td>Proprietà avanzate non specifiche dell'hardware.
<blockquote>
[!Note]<br />
Questa operazione non è più supportata in Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Impostazioni di visualizzazione avanzate</td>
<td>Visualizza</td>
<td>Proprietà avanzate specifiche dell'hardware.
<blockquote>
[!Note]<br />
Questa operazione non è più supportata in Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Opzioni Internet</td>
<td>Internet</td>
<td>Il numero massimo di pagine di estensione è 18.</td>
</tr>
<tr class="odd">
<td>Tastiera</td>
<td>Tastiera</td>
<td>Il numero massimo di pagine di estensione è 30.</td>
</tr>
<tr class="even">
<td>Mouse</td>
<td>Mouse</td>
<td>Supporta anche la sostituzione di pagine standard. Il numero massimo di pagine di estensione è 8.</td>
</tr>
<tr class="odd">
<td>Opzioni risparmio energia</td>
<td>Potenza</td>
<td>Il numero massimo di pagine, incluse le pagine standard, è 18.</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Sistema</td>
<td>Il numero massimo di pagine di estensione è 8.
<blockquote>
[!Note]<br />
Questa operazione non è più supportata in Windows Vista.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

L'elemento **Installazione applicazioni** nel pannello di controllo di Windows XP non è una finestra delle proprietà e pertanto non può essere esteso dai metodi descritti qui. Il relativo contenuto viene invece ottenuto dagli autori dell'applicazione. Per ulteriori informazioni sull'aggiunta di contenuto per l'aggiunta **o la rimozione di programmi**, vedere [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Elaborazione del messaggio del pannello di controllo](message-processing.md)
</dt> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




