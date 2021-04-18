---
description: Il registro di sistema contiene i dati di configurazione usati dal sistema operativo, dai servizi e dalle applicazioni.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modifica del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305578"
---
# <a name="modifying-the-system-registry"></a>Modifica del registro di sistema

Il registro di sistema contiene i dati di configurazione usati dal sistema operativo, dai servizi e dalle applicazioni. Strumentazione gestione Windows (WMI) dispone di un [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) con metodi che consentono di monitorare o modificare il registro di sistema nel computer locale o nei computer remoti. Il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) supporta la classe del [**\_ Registro di sistema Win32**](/windows/desktop/CIMWin32Prov/win32-registry) che contiene dati statici sulle dimensioni di un registro.

Il provider del registro di sistema è un'istanza, una proprietà e un provider di eventi che si interfacciano con il registro di sistema. Il provider del registro di sistema è un provider standard con l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . È possibile utilizzare il provider del registro di sistema per accedere alle chiavi del registro di sistema e alle informazioni sui sistemi locali e remoti. Per ulteriori informazioni, vedere [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI inserisce [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) nello \\ spazio dei nomi predefinito radice. Tuttavia, è possibile compilare il file regevent. mof in altri spazi dei nomi per l'uso da parte di altre applicazioni.

Gli argomenti descritti nella tabella seguente illustrano come usare la classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e il provider del registro di sistema.



| Argomento                                                                                              | Descrizione                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recupero dei dati del registro di sistema](obtaining-registry-data.md)                                             | È possibile ottenere o modificare i dati del registro di sistema tramite i metodi della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) , che consente di automatizzare le attività del registro di sistema in locale o in remoto.                    |
| [Modifica dei dati del registro di sistema](changing-registry-data.md)                                               | È possibile aggiungere o eliminare chiavi e aggiungere o modificare i valori delle voci del registro di sistema in chiavi.                                                                                                                    |
| [Programmazione con il provider del registro di sistema](programming-with-the-system-registry-provider.md) | È possibile definire classi personalizzate fornite dal registro di sistema con i dati.                                                                                                                       |
| [Registrazione per eventi registro di sistema](registering-for-system-registry-events.md)               | Il provider del registro di sistema può inviare eventi a un consumer. Per ricevere gli eventi, è necessario registrare il consumer, creare una query e quindi assicurarsi che il provider invii gli eventi, in modo corretto. |
| [Registrazione del provider del registro di sistema](registering-the-system-registry-provider.md)           | Il provider del registro di sistema viene registrato come parte del processo di installazione di WMI.                                                                                                                |



 

 

 
