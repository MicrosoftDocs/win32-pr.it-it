---
description: Le funzioni seguenti vengono utilizzate con MUI (Multilingual User Interface).
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: Funzioni dell'interfaccia utente multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f082115b0b12bdf6d26923ed8fc941b89887723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130306"
---
# <a name="multilingual-user-interface-functions"></a>Funzioni dell'interfaccia utente multilingue

Le funzioni seguenti vengono utilizzate con MUI (Multilingual User Interface).



| Funzione                                                                 | Descrizione                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | Enumera le lingue dell'interfaccia utente disponibili nel sistema operativo.                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | Funzione definita dall'applicazione utilizzata con la funzione [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .                      |
| [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | Decrementa il conteggio dei riferimenti di un modulo di risorse caricato da [ **LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**GetFileMUIInfo**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | Recupera le informazioni correlate alle risorse relative a un file.                                                                    |
| [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | Recupera il percorso di un file di risorse specifico della lingua associato al file.                           |
| [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | Recupera le lingue dell'interfaccia utente preferite del processo.                                                                           |
| [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | Recupera l'identificatore di lingua per la lingua dell'interfaccia utente predefinita del sistema, nota come "lingua di installazione" in Windows Vista. |
| [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | Recupera le lingue dell'interfaccia utente preferite del sistema.                                                                            |
| [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | Recupera le lingue dell'interfaccia utente preferite per il thread corrente.                                                     |
| [**GetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | Restituisce l'identificatore di lingua della prima lingua dell'interfaccia utente per il thread corrente.                            |
| [**GetUILanguageFallbackList**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | Ottiene un elenco di fallback di lingue dell'interfaccia utente rappresentate come nomi di lingua.                                         |
| [**GetUILanguageInfo**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | Recupera una serie di informazioni su una lingua dell'interfaccia utente.                                                     |
| [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | Restituisce l'identificatore di lingua per la lingua dell'interfaccia utente dell'utente corrente.                                          |
| [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | Recupera le lingue dell'interfaccia utente preferite dell'utente.                                                                              |
| [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | Restituisce un handle per le risorse specifiche della lingua associate a un file specifico indipendente dalla lingua (LN).            |
| [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | Imposta le lingue dell'interfaccia utente preferite del processo per il processo dell'applicazione.                                                    |
| [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | Imposta le lingue dell'interfaccia utente preferite del thread.                                                                                 |
| [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | Imposta la lingua dell'interfaccia utente preferita per il thread corrente.                                                      |



 

 

 
