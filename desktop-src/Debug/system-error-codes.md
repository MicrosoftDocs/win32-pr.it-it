---
description: Fornisce collegamenti ai codici di errore di sistema definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Codici di errore di sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 4c762b2098531ecb19ad84522f8c9c8272c004397bbc4b32f15a6f6e157c4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691731"
---
# <a name="system-error-codes"></a>Codici di errore di sistema

Questa sezione è destinata agli sviluppatori che ese tracciano errori di sistema. Se è stata raggiunta questa pagina durante la ricerca di altri errori, ecco alcuni collegamenti che potrebbero essere utili:

* [Windows errori di aggiornamento:](https://support.microsoft.com/help/10164/fix-windows-update-errors) per risolvere i problemi relativi Windows Update.
* [Windows errori di attivazione:](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) per informazioni sulla verifica della copia di Windows.
* [Risoluzione degli errori della schermata blu:](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) per informazioni su ciò che ha causato un errore di arresto.
* [Supporto tecnico Microsoft:](https://support.microsoft.com) per il supporto con un prodotto Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Altri modi per trovare un codice di errore

In questa sezione sono elencati i codici di errore di sistema, organizzati in base al numero. Per altre informazioni sul rilevamento di un errore specifico, ecco alcune raccomandazioni:

* Usare lo [strumento Di ricerca errori Microsoft](system-error-code-lookup-tool.md).
*  Installare gli strumenti di debug per Windows, caricare un file di dump della memoria e quindi eseguire il **\! comando err. \<code>**
* Cercare il testo non elaborato o il codice di errore nel sito Dei protocolli Microsoft. Per altre informazioni, vedere [[MS-ERREF]: Windows di errore](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Codici di errore di terze parti

Altri codici di errore possono essere generati da servizi o app di terze parti (ad esempio, codice di **errore: -118** può essere visualizzato dal servizio di gioco [di Steam)](https://support.steampowered.com/kb_cat.php?id=59)e in questi casi si potrebbe contattare la riga di supporto di terze parti.

## <a name="system-error-codes"></a>Codici di errore di sistema

I codici di errore di sistema sono molto ampi: ognuno può verificarsi in una delle centinaia di posizioni del sistema. Di conseguenza, le descrizioni di questi codici non possono essere molto specifiche. L'uso di questi codici richiede una certa quantità di analisi e analisi. È necessario prendere nota sia del contesto a livello di codice che del contesto di runtime in cui si verificano questi errori. 

Poiché questi codici sono definiti in WinError.h per tutti gli utenti, talvolta i codici vengono restituiti da software non di sistema. E talvolta il codice viene restituito da una funzione in profondità nello stack e lontano dal codice che gestisce l'errore.

Negli argomenti seguenti vengono forniti elenchi di codici di errore di sistema. Questi valori sono definiti nel file di intestazione WinError.h.

-   [Codici di errore di sistema (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Codici di errore di sistema (500-999) (0x1f4-0x3e7)](system-error-codes--500-999-.md)
-   [Codici di errore di sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Codici di errore di sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Codici di errore di sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Codici di errore di sistema (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Codici di errore di sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Codici di errore di sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Codici di errore di sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Codici di errore di sistema (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
