---
description: Un hive è un gruppo logico di chiavi, sottochiavi e valori nel registro di sistema che dispone di un set di file di supporto che contengono backup dei dati.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Hive del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882346"
---
# <a name="registry-hives"></a>Hive del registro di sistema

Un *hive* è un gruppo logico di chiavi, sottochiavi e valori nel registro di sistema che dispone di un set di file di supporto caricati in memoria quando viene avviato il sistema operativo o un utente esegue l'accesso.

Ogni volta che un nuovo utente accede a un computer, viene creato un nuovo hive per tale utente con un file separato per il profilo utente. Questa operazione è denominata *hive del profilo utente*. L'hive di un utente contiene informazioni specifiche sul Registro di sistema relative alle impostazioni dell'applicazione, al desktop, all'ambiente, alle connessioni di rete e alle stampanti dell'utente. Gli hive dei profili utente si trovano nella **chiave \_ utenti HKEY** .

I file del registro di sistema presentano i due formati seguenti: standard e più recente. Il formato standard è l'unico formato supportato da Windows 2000. È inoltre supportata da versioni successive di Windows per la compatibilità con le versioni precedenti. Il formato più recente è supportato a partire da Windows XP. Nelle versioni di Windows che supportano il formato più recente, gli hive seguenti usano ancora il formato standard: **HKEY \_ Current \_ User**, **HKEY \_ Local \_ computer \\ Sam**, **HKEY \_ Local \_ computer \\ Security** e **HKEY \_ Users \\ . Impostazione predefinita**; tutti gli altri hive usano il formato più recente.

La maggior parte dei file di supporto per gli hive si trova nella directory% SystemRoot% \\ system32 \\ config. Questi file vengono aggiornati ogni volta che un utente esegue l'accesso. Le estensioni dei nomi di file in queste directory o, in alcuni casi, una mancanza di estensione, indicano il tipo di dati che contengono. La tabella seguente elenca queste estensioni insieme a una descrizione dei dati nel file.



| Estensione       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno<br/> | Copia completa dei dati hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Alt<br/> | Una copia di backup dell'hive critico del **\_ \_ \\ sistema locale del computer HKEY** . Solo la chiave di sistema ha un file con estensione ALT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Un log delle transazioni delle modifiche alle chiavi e alle voci di valore in hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| . sav<br/> | Una copia di backup di un hive.<br/> **Windows Server 2003 e Windows XP/2000:** Copie dei file hive esaminate alla fine della fase in modalità testo nel programma di installazione. Il programma di installazione è costituito da due fasi: modalità testo e modalità grafica. L'hive viene copiato in un file con estensione SAV dopo la fase in modalità testo del programma di installazione per proteggerlo da errori che potrebbero verificarsi se la fase della modalità grafica del programma di installazione ha esito negativo. Se l'installazione non riesce durante la fase della modalità grafica, solo la fase della modalità grafica viene ripetuta quando il computer viene riavviato; il file. sav viene usato per ripristinare i dati hive.<br/> |



 

La tabella seguente elenca gli hive standard e i relativi file di supporto.



| Hive del registro di sistema                      | File di supporto                           |
|------------------------------------|--------------------------------------------|
| **HKEY \_ \_ configurazione corrente**          | System, System. Alt, System. log, System. sav |
| **HKEY \_ \_ utente corrente**            | Ntuser. dat, Ntuser. dat. log                 |
| **\_ \_ Sam computer locale \\ HKEY**      | Sam, Sam. log, Sam. sav                      |
| **\_Sicurezza del \_ computer \\ locale HKEY** | Security, Security. log, Security. sav       |
| **\_Software del \_ computer \\ locale HKEY** | Software, software. log, software. sav       |
| **\_Sistema del \_ computer \\ locale HKEY**   | System, System. Alt, System. log, System. sav |
| **\_utenti HKEY \\ . PREDEFINITA**          | Default. log, default. sav          |



 

 

 




