---
description: Alcuni degli elementi di sistema trovati nel Pannello di controllo sono estendibili. Per installare un'Pannello di controllo, registrare l'estensione shell come indicato di seguito, dove nome è il nome predefinito dell'elemento di sistema (vedere la tabella seguente).
title: Estensione degli elementi di Pannello di controllo sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469748"
---
# <a name="extending-system-control-panel-items"></a>Estensione degli elementi di Pannello di controllo sistema

Alcuni degli elementi di sistema trovati nel Pannello di controllo sono estendibili. Per installare un'Pannello di controllo, registrare l'estensione shell come indicato di seguito, dove *nome* è il nome predefinito dell'elemento di sistema (vedere la tabella seguente).

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

Questo è simile al modo in cui si registra un'estensione per un oggetto Shell predefinito. Poiché le uniche estensioni della shell supportate Pannello di controllo elementi sono finestre delle proprietà, la registrazione deve essere nella **sottochiave** \\ **shellex PropertySheetHandlers.**




| Pannello di controllo elemento | <em>nome</em> | Commenti | 
|--------------------|---------------|---------|
| Visualizza | Scrivania | Supporta anche la sostituzione della <strong>pagina Desktop.</strong><blockquote>[!Note]<br />Questa funzionalità non è più supportata in Windows Vista.</blockquote><br /> | 
| Visualizzazione Impostazioni avanzate | Dispositivo | Proprietà avanzate non specifiche delhardware.<blockquote>[!Note]<br />Questa funzionalità non è più supportata in Windows Vista.</blockquote><br /> | 
| Visualizzazione Impostazioni avanzate | Visualizza | Proprietà avanzate specifiche dell'hardware.<blockquote>[!Note]<br />Questa funzionalità non è più supportata in Windows Vista.</blockquote><br /> | 
| Opzioni Internet | Internet | Il numero massimo di pagine di estensione è 18. | 
| Tastiera | Tastiera | Il numero massimo di pagine di estensione è 30. | 
| Mouse | Mouse | Supporta anche la sostituzione delle pagine standard. Il numero massimo di pagine di estensione è 8. | 
| Opzioni risparmio energia | Elettricità | Il numero massimo di pagine, incluse le pagine standard, è 18. | 
| Sistema | Sistema | Il numero massimo di pagine di estensione è 8.<blockquote>[!Note]<br />Questa funzionalità non è più supportata in Windows Vista.</blockquote><br /> | 




 

**L'elemento Installazione** applicazioni nel Windows XP Pannello di controllo non è una finestra delle proprietà e pertanto non può essere esteso dai metodi descritti qui. Il contenuto viene invece ottenuto dagli editori di applicazioni. Per altre informazioni sull'aggiunta di contenuto **a** Installazione applicazioni, vedere [**IAppPublisher,**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher) [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp.**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in modalità Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




