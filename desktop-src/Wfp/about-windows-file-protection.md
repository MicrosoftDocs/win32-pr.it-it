---
description: Windows Protezione risorse impedisce la sostituzione di file di sistema, cartelle e chiavi del Registro di sistema essenziali installati come parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informazioni Windows delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134199"
---
# <a name="about-windows-resource-protection"></a>Informazioni Windows delle risorse

Windows Protezione risorse impedisce la sostituzione di file di sistema, cartelle e chiavi del Registro di sistema essenziali installati come parte del sistema operativo. È diventato disponibile a partire da Windows Server 2008 e Windows Vista. L'autorizzazione per l'accesso completo per modificare le risorse protette da WRP è limitata a TrustedInstaller. Le risorse protette da WRP possono essere modificate solo usando [i meccanismi](supported-file-replacement-mechanisms.md) di sostituzione delle risorse supportati con il Windows di installazione dei moduli. La protezione di queste risorse impedisce errori dell'applicazione e del sistema operativo.

Le applicazioni non devono tentare di modificare le risorse protette da WRP perché vengono usate da Windows e altre applicazioni. Se un'applicazione tenta di modificare una risorsa protetta da WRP, può ottenere i risultati seguenti.

-   I programmi di installazione delle applicazioni che tentano di sostituire, modificare o eliminare i file Windows critici o le chiavi del Registro di sistema potrebbero non riuscire a installare l'applicazione e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.
-   Le applicazioni che tentano di aggiungere o rimuovere chiavi secondarie o di modificare i valori delle chiavi del Registro di sistema protette potrebbero non riuscire e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.
-   Le applicazioni che si basano sulla scrittura di informazioni in chiavi, cartelle o file del Registro di sistema protetti potrebbero non riuscire.

WRP è il nuovo nome per Windows protezione file (WFP). WRP protegge le chiavi e le cartelle del Registro di sistema, nonché i file di sistema essenziali. WFP era disponibile in Microsoft Windows Server 2003 e Windows XP. WRP sostituisce WFP in Windows Server 2008 e Windows Vista.

Gli argomenti seguenti descrivono WRP:

-   [Elenco di risorse protette](protected-file-list.md)
-   [Rilevamento della sostituzione delle risorse](detecting-file-replacement.md)
-   [Meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md)
-   [Verifica file di sistema](system-file-checker.md)
-   [Considerazioni sull'amministrazione remota](remote-administration-considerations.md)

 

 



