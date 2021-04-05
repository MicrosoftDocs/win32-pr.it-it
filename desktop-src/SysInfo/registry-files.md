---
description: Le applicazioni possono salvare parte del registro di sistema in un file e quindi caricare nuovamente il contenuto del file nel registro di sistema.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: File del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44916618946f6541495186aa5843799c9b864fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967667"
---
# <a name="registry-files"></a>File del registro di sistema

Le applicazioni possono salvare parte del registro di sistema in un file e quindi caricare nuovamente il contenuto del file nel registro di sistema. Un file del registro di sistema è utile quando viene modificata una grande quantità di dati, quando vengono eseguite molte voci nel registro di sistema o quando i dati sono transitori e devono essere caricati e quindi scaricati di nuovo. È probabile che le applicazioni che eseguono il backup e il ripristino di parti del registro di sistema usino i file del registro di sistema.

Per salvare una chiave e le relative sottochiavi e valori in un file del registro di sistema, un'applicazione può chiamare la funzione [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) o [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) .

[**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) e [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) creano il file con l'attributo Archive. Il file viene creato nella directory corrente del processo per una chiave locale e nella directory% SystemRoot% \\ system32 per una chiave remota.

I file del registro di sistema presentano i due formati seguenti: standard e più recente. Il formato standard è l'unico formato supportato da Windows 2000. È inoltre supportata da versioni successive di Windows per la compatibilità con le versioni precedenti. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) crea file nel formato standard.

Il formato più recente è supportato a partire da Windows XP. I file del registro di sistema creati in questo formato non possono essere caricati in Windows 2000. [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) consente di salvare i file del registro di sistema in entrambi i formati specificando il formato reg \_ standard \_ o reg \_ Latest \_ . Pertanto, può essere usato per convertire i file del registro di sistema che usano il formato standard nel formato più recente.

Per scrivere nuovamente il file del registro di sistema nel registro di sistema, un'applicazione può utilizzare le funzioni [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)o [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) come indicato di seguito.

-   **RegLoadKey** carica i dati del registro di sistema da un file specificato in una sottochiave specificata in **HKEY \_ Users** o **HKEY \_ Local \_** computer nel computer dell'applicazione chiamante o in un computer remoto. La funzione crea la sottochiave specificata, se non esiste già. Dopo la chiamata a questa funzione, un'applicazione può utilizzare la funzione [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) per ripristinare lo stato precedente del registro di sistema.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) sostituisce una chiave e tutte le sottochiavi e i valori nel registro di sistema con i dati contenuti in un file specificato. I nuovi dati vengono applicati al successivo avvio del sistema.
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) carica i dati del registro di sistema da un file specificato in una chiave specificata nel computer dell'applicazione chiamante o in un computer remoto. Questa funzione sostituisce le sottochiavi e i valori al di sotto della chiave specificata con le sottochiavi e i valori che seguono la chiave di primo livello nel file.

La funzione [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) stabilisce una connessione a un handle del registro di sistema predefinito in un altro computer. Un'applicazione utilizza questa funzione principalmente per accedere alle informazioni da un registro di sistema remoto in altri computer in un ambiente di rete, operazione che può essere eseguita anche tramite l'editor del registro di sistema. Potrebbe essere necessario accedere a un registro di sistema remoto per eseguire il backup di un registro di sistema o regolarne l'accesso alla rete. Si noti che è necessario disporre delle autorizzazioni appropriate per accedere a un registro di sistema remoto tramite questa funzione.

 

 



