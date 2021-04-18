---
description: Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informazioni su Protezione risorse di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317026"
---
# <a name="about-windows-resource-protection"></a>Informazioni su Protezione risorse di Windows

Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo. È diventato disponibile a partire da Windows Server 2008 e Windows Vista. L'autorizzazione per l'accesso completo per modificare le risorse protette con WRP è limitata a TrustedInstaller. Le risorse protette da WRP possono essere modificate solo usando i [meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md) con il servizio moduli di installazione di Windows. La protezione di queste risorse impedisce gli errori dell'applicazione e del sistema operativo.

Le applicazioni non devono tentare di modificare le risorse protette da WRP perché vengono usate da Windows e da altre applicazioni. Se un'applicazione tenta di modificare una risorsa protetta da WRP, può presentare i risultati seguenti.

-   I programmi di installazione di applicazioni che tentano di sostituire, modificare o eliminare file di Windows critici o chiavi del registro di sistema potrebbero non essere in grado di installare l'applicazione e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.
-   Le applicazioni che tentano di aggiungere o rimuovere sottochiavi o modificare i valori delle chiavi del registro di sistema protette potrebbero avere esito negativo e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.
-   Le applicazioni che si basano sulla scrittura di informazioni in chiavi del registro di sistema protette, cartelle o file potrebbero avere esito negativo.

WRP è il nuovo nome per la protezione dei file di Windows (WFP). WRP protegge le chiavi del registro di sistema e le cartelle, nonché i file di sistema essenziali. Pam era disponibile in Microsoft Windows Server 2003 e Windows XP. WRP sostituisce WFP in Windows Server 2008 e Windows Vista.

Gli argomenti seguenti descrivono WRP:

-   [Elenco delle risorse protette](protected-file-list.md)
-   [Rilevamento della sostituzione delle risorse](detecting-file-replacement.md)
-   [Meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md)
-   [Controllo file di sistema](system-file-checker.md)
-   [Considerazioni sull'amministrazione remota](remote-administration-considerations.md)

 

 



