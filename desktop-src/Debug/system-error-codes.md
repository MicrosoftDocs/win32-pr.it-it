---
description: Fornisce collegamenti a codici di errore di sistema definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Codici di errore di sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126828"
---
# <a name="system-error-codes"></a>Codici di errore di sistema

Questa sezione è destinata agli sviluppatori che eseguono il debug degli errori di sistema. Se è stata raggiunta questa pagina durante la ricerca di altri errori, di seguito sono riportati alcuni collegamenti che possono risultare utili:

* [Windows Update errori](https://support.microsoft.com/help/10164/fix-windows-update-errors) : per informazioni sulla risoluzione dei problemi relativi a Windows Update.
* [Errori di attivazione di Windows](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) : per informazioni sulla verifica della copia di Windows.
* [Risoluzione degli errori di schermata blu](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) : per informazioni sull'individuazione di un errore irreversibile.
* [Supporto tecnico Microsoft](https://support.microsoft.com) per il supporto di un prodotto Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Altri modi per trovare un codice di errore

In questa sezione sono stati elencati i codici di errore di sistema organizzati per numero. Per ulteriori informazioni su come tenere traccia di un errore specifico, di seguito sono riportate alcune indicazioni:

* Utilizzare lo [strumento ricerca errori Microsoft](system-error-code-lookup-tool.md).
*  Installare gli strumenti di debug per Windows, caricare un file di dump della memoria, quindi eseguire il comando **\! Err \<code>** .
* Cercare il testo non elaborato o il codice di errore nel sito dei protocolli Microsoft. Per ulteriori informazioni, vedere [[MS-ERREF]: codici di errore di Windows](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Codici di errore di terze parti

Altri codici di errore possono essere generati da app o servizi di terze parti (ad esempio, il **codice di errore:-118** può essere visualizzato dal [servizio gioco di Steam](https://support.steampowered.com/kb_cat.php?id=59)) e in tali situazioni è necessario contattare la linea di supporto di terze parti.

## <a name="system-error-codes"></a>Codici di errore di sistema

I codici di errore di sistema sono molto ampi, ognuno dei quali può verificarsi in una delle numerose centinaia di posizioni del sistema. Di conseguenza, le descrizioni di questi codici non possono essere molto specifiche. L'uso di questi codici richiede una certa quantità di analisi e analisi. È necessario prendere nota sia del contesto programmatico che del contesto di runtime in cui si verificano questi errori. 

Poiché questi codici sono definiti in WinError. h per consentire l'utilizzo da parte di chiunque, a volte i codici vengono restituiti dal software non di sistema. A volte il codice viene restituito da una funzione in profondità nello stack ed è stato rimosso dal codice che gestisce l'errore.

Negli argomenti seguenti vengono forniti elenchi di codici di errore di sistema. Questi valori vengono definiti nel file di intestazione WinError. h.

-   [Codici di errore di sistema (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Codici di errore di sistema (500-999) (0x1F4-0x3E7)](system-error-codes--500-999-.md)
-   [Codici di errore di sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Codici di errore di sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Codici di errore di sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Codici di errore di sistema (4000-5999) (0xFA0-0x176f)](system-error-codes--4000-5999-.md)
-   [Codici di errore di sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Codici di errore di sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Codici di errore di sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Codici di errore di sistema (12000-15999) (0x2EE0-0x3e7f)](system-error-codes--12000-15999-.md)
