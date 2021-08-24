---
description: Le tabelle dei messaggi sono risorse stringa speciali usate per la visualizzazione dei messaggi di errore. Vengono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa MESSAGETABLE. Per accedere alle stringhe di messaggio, usare la funzione FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tabelle dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691821"
---
# <a name="message-tables"></a>Tabelle dei messaggi

Le tabelle dei messaggi sono risorse stringa speciali usate per la visualizzazione dei messaggi di errore. Vengono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa [MESSAGETABLE.](../menurc/messagetable-resource.md) Per accedere alle stringhe di messaggio, usare la [**funzione FormatMessage.**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)

Il sistema fornisce una tabella di messaggi per i codici [di errore di sistema](system-error-codes.md). Per recuperare la stringa corrispondente al codice di errore, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM \_ \_ SYSTEM.

Per fornire una tabella dei messaggi per l'applicazione, seguire le istruzioni in [File di testo dei messaggi](../eventlog/message-text-files.md). Per recuperare stringhe dalla tabella dei messaggi, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM \_ \_ HMODULE.

 

 
