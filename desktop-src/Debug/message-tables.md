---
description: Le tabelle messaggi sono risorse di stringa speciali utilizzate per la visualizzazione dei messaggi di errore. Sono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa MESSAGETABLE. Per accedere alle stringhe di messaggio, usare la funzione FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tabelle messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965943"
---
# <a name="message-tables"></a>Tabelle messaggi

Le tabelle messaggi sono risorse di stringa speciali utilizzate per la visualizzazione dei messaggi di errore. Sono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa [MESSAGETABLE](../menurc/messagetable-resource.md) . Per accedere alle stringhe di messaggio, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

Il sistema fornisce una tabella dei messaggi per i [codici di errore di sistema](system-error-codes.md). Per recuperare la stringa che corrisponde al codice di errore, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il \_ messaggio \_ di formato dal \_ flag di sistema.

Per fornire una tabella dei messaggi per l'applicazione, seguire le istruzioni riportate in [file di testo dei messaggi](../eventlog/message-text-files.md). Per recuperare le stringhe dalla tabella messaggi, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il \_ messaggio Format \_ dal \_ flag HMODULE.

 

 
