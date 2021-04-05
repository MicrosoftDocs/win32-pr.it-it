---
description: SCM gestisce un database dei servizi installati nel registro di sistema.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Database dei servizi installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968195"
---
# <a name="database-of-installed-services"></a>Database dei servizi installati

SCM gestisce un database dei servizi installati nel registro di sistema. Il database viene utilizzato da SCM e programmi che aggiungono, modificano o configurano i servizi. Di seguito è riportata la chiave del registro di sistema per il database: **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**.

Questa chiave contiene una sottochiave per ogni servizio installato e per il servizio driver. Il nome della sottochiave è il nome del servizio, come specificato dalla funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) quando il servizio è stato installato da un programma di configurazione del servizio.

Quando il sistema viene installato, viene creata una copia iniziale del database. Il database contiene le voci per i driver di dispositivo necessari durante l'avvio del sistema. Nel database sono incluse le seguenti informazioni su ogni servizio installato e servizio driver:

-   Tipo di servizio. Indica se il servizio viene eseguito nel proprio processo o condivide un processo con altri servizi. Per servizi driver, indica se il servizio è un driver del kernel o un driver file system.
-   Tipo di avvio. Indica se il servizio o il servizio driver viene avviato automaticamente all'avvio del sistema (servizio di avvio automatico) o se il servizio SCM lo avvia quando richiesto da un programma di controllo del servizio (servizio di avvio della richiesta). Il tipo di avvio può indicare anche che il servizio o il servizio driver è disabilitato, nel qual caso non può essere avviato.
-   Livello di controllo degli errori. In questo modo viene specificata la gravità dell'errore se il servizio o il servizio driver non viene avviato durante l'avvio del sistema e determina l'azione che verrà eseguita dal programma di avvio.
-   Percorso completo del file eseguibile. L'estensione del nome file è. EXE per i servizi e. SYS per i servizi del driver.
-   Informazioni facoltative sulle dipendenze utilizzate per determinare l'ordine corretto per l'avvio dei servizi o dei servizi del driver. Per i servizi di, queste informazioni possono includere un elenco di servizi che SCM deve avviare prima di poter avviare il servizio specificato, il nome di un gruppo di ordini di carico di cui fa parte il servizio e un identificatore di tag che indica l'ordine di avvio del servizio nel relativo gruppo di ordini di carico. Per i servizi driver, queste informazioni includono un elenco di driver che devono essere avviati prima del driver specificato.
-   Per i servizi, un nome account e una password facoltativi. Il programma del servizio viene eseguito nel contesto di questo account. Se non viene specificato alcun account, il servizio viene eseguito nel contesto dell' [account LocalSystem](localsystem-account.md).
-   Per i servizi driver, un nome di oggetto driver facoltativo, ad esempio \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema i/O per caricare il driver di dispositivo. Se non si specifica alcun nome, il sistema di I/O crea un nome predefinito in base al nome del servizio driver.

> [!Note]  
> Questo database è noto anche come database ServicesActive o SCM. È necessario utilizzare le funzioni fornite da SCM, anziché modificare direttamente il database.

 

 

 



