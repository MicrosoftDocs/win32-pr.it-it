---
description: Un hive è un gruppo logico di chiavi, sottochiavi e valori nel Registro di sistema che include un set di file di supporto contenenti backup dei relativi dati.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Hive del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11920a7b70a8aeb78b08aee2c25b89c4de5457b5cb96a480fc1f75fff6c6a35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763628"
---
# <a name="registry-hives"></a>Hive del Registro di sistema

Un *hive* è un gruppo logico di chiavi, sottochiavi e valori nel Registro di sistema con un set di file di supporto caricati in memoria all'avvio del sistema operativo o all'accesso di un utente.

Ogni volta che un nuovo utente accede a un computer, viene creato un nuovo hive per tale utente con un file separato per il profilo utente. Si tratta *dell'hive del profilo utente*. L'hive di un utente contiene informazioni specifiche del Registro di sistema relative alle impostazioni dell'applicazione, al desktop, all'ambiente, alle connessioni di rete e alle stampanti dell'utente. Gli hive del profilo utente si trovano nella **chiave HKEY \_ USERS.**

I file del Registro di sistema hanno i due formati seguenti: standard e più recente. Il formato standard è l'unico formato supportato da Windows 2000. È supportato anche dalle versioni successive di Windows per la compatibilità con le versioni precedenti. Il formato più recente è supportato a partire da Windows XP. Nelle versioni di Windows che supportano il formato più recente, gli hive seguenti usano ancora il formato standard: **HKEY \_ CURRENT \_ USER,** **HKEY \_ LOCAL MACHINE \_ \\ SAM,** **HKEY LOCAL MACHINE \_ \_ \\ Security** e **HKEY USERS \_ \\ . DEFAULT**; Tutti gli altri hive usano il formato più recente.

La maggior parte dei file di supporto per gli hive si tratta della directory %SystemRoot% \\ System32 \\ Config. Questi file vengono aggiornati ogni volta che un utente accede. Le estensioni di file dei file in queste directory, o in alcuni casi la mancanza di un'estensione, indicano il tipo di dati che contengono. Nella tabella seguente sono elencate queste estensioni insieme a una descrizione dei dati nel file.



| Estensione       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno<br/> | Copia completa dei dati hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| .alt<br/> | Copia di backup dell'hive **di sistema \_ HKEY LOCAL \_ MACHINE \\** critico. Solo la chiave di sistema ha un file con estensione alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Log delle transazioni delle modifiche alle chiavi e alle voci di valore nell'hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| .sav<br/> | Copia di backup di un hive.<br/> **Windows Server 2003 e Windows XP/2000:** Copie dei file hive mentre si guardavano alla fine della fase in modalità testo nel programma di installazione. Il programma di installazione ha due fasi: modalità testo e modalità grafica. L'hive viene copiato in un file con estensione sav dopo la fase di configurazione in modalità testo per proteggerlo da errori che potrebbero verificarsi se la fase della modalità grafica dell'installazione non riesce. Se l'installazione non riesce durante la fase della modalità grafica, al riavvio del computer viene ripetuta solo la fase della modalità grafica. Il file con estensione sav viene usato per ripristinare i dati hive.<br/> |



 

Nella tabella seguente sono elencati gli hive standard e i relativi file di supporto.



| Hive del Registro di sistema                      | File di supporto                           |
|------------------------------------|--------------------------------------------|
| **HKEY \_ CURRENT \_ CONFIG**          | System, System.alt, System.log, System.sav |
| **HKEY \_ CURRENT \_ USER**            | Ntuser.dat, Ntuser.dat.log                 |
| **HKEY \_ LOCAL \_ MACHINE \\ SAM**      | Sam, Sam.log, Sam.sav                      |
| **Sicurezza HKEY \_ LOCAL \_ MACHINE \\** | Security, Security.log, Security.sav       |
| **HKEY \_ LOCAL \_ MACHINE \\ Software** | Software, Software.log, Software.sav       |
| **HKEY \_ LOCAL \_ MACHINE \\ System**   | System, System.alt, System.log, System.sav |
| **HKEY \_ USERS \\ . Predefinito**          | Default, Default.log, Default.sav          |



 

 

 




