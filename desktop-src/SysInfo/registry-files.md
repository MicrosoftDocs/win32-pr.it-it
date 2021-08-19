---
description: Le applicazioni possono salvare parte del Registro di sistema in un file e quindi caricare nuovamente il contenuto del file nel Registro di sistema.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: File del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a5caa34a075e4bffe48a542d02eec896ab28dd93fbdc2745dbc5a08effb9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763814"
---
# <a name="registry-files"></a>File del Registro di sistema

Le applicazioni possono salvare parte del Registro di sistema in un file e quindi caricare nuovamente il contenuto del file nel Registro di sistema. Un file del Registro di sistema è utile quando viene manipolata una grande quantità di dati, quando vengono apportate molte voci nel Registro di sistema o quando i dati sono transitori e devono essere caricati e quindi scaricati nuovamente. È probabile che le applicazioni che eseranno il backup e il ripristino di parti del Registro di sistema usino file del Registro di sistema.

Per salvare una chiave e le relative sottochiavi e valori in un file del Registro di sistema, un'applicazione può chiamare la funzione [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) o [**RegSaveKeyEx.**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)

[**RegSaveKey e**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) [**RegSaveKeyEx creano**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) il file con l'attributo archive. Il file viene creato nella directory corrente del processo per una chiave locale e nella directory %systemroot% \\ system32 per una chiave remota.

I file del Registro di sistema hanno i due formati seguenti: standard e più recente. Il formato standard è l'unico formato supportato da Windows 2000. È supportato anche dalle versioni successive di Windows per la compatibilità con le versioni precedenti. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) crea file nel formato standard.

Il formato più recente è supportato a partire da Windows XP. I file del Registro di sistema creati in questo formato non possono essere caricati in Windows 2000. [**RegSaveKeyEx può**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) salvare i file del Registro di sistema in entrambi i formati specificando REG \_ STANDARD FORMAT o REG LATEST \_ \_ \_ FORMAT. Pertanto, può essere usato per convertire i file del Registro di sistema che usano il formato standard nel formato più recente.

Per scrivere di nuovo il file del Registro di sistema nel Registro di sistema, un'applicazione può usare le funzioni [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)o [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) come indicato di seguito.

-   **RegLoadKey carica** i dati del Registro di sistema da un file specificato in una sottochiave specificata in **HKEY \_ USERS** o **HKEY \_ LOCAL \_ MACHINE** nel computer dell'applicazione chiamante o in un computer remoto. La funzione crea la sottochiave specificata, se non esiste già. Dopo aver chiamato questa funzione, un'applicazione può usare la [**funzione RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) per ripristinare lo stato precedente del Registro di sistema.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) sostituisce una chiave e tutte le relative sottochiavi e valori nel Registro di sistema con i dati contenuti in un file specificato. I nuovi dati vengono applicate al successivo avvio del sistema.
-   [**RegRestoreKey carica**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) i dati del Registro di sistema da un file specificato in una chiave specificata nel computer dell'applicazione chiamante o in un computer remoto. Questa funzione sostituisce le sottochiavi e i valori sotto la chiave specificata con le sottochiavi e i valori che seguono la chiave di primo livello nel file.

La [**funzione RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) stabilisce una connessione a un handle del Registro di sistema predefinito in un altro computer. Un'applicazione usa questa funzione principalmente per accedere alle informazioni da un registro remoto in altri computer in un ambiente di rete, operazione che è possibile eseguire anche usando l'editor del Registro di sistema. Potrebbe essere necessario accedere a un registro remoto per eseguire il backup di un registro o regolare l'accesso di rete a esso. Si noti che è necessario disporre delle autorizzazioni appropriate per accedere a un registro remoto usando questa funzione.

 

 



