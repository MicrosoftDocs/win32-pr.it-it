---
description: Il Registro di sistema contiene i dati di configurazione utilizzati dal sistema operativo, i servizi e le applicazioni.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modifica del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33562e2747d63d8531ff2b23d07eadac33d830ef3ecf3b8613f22170c0b735ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992841"
---
# <a name="modifying-the-system-registry"></a>Modifica del Registro di sistema

Il Registro di sistema contiene i dati di configurazione utilizzati dal sistema operativo, i servizi e le applicazioni. Windows Strumentazione gestione (WMI) include un [provider](/previous-versions/windows/desktop/regprov/system-registry-provider) del Registro di sistema e la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) con metodi che usano per monitorare o modificare il Registro di sistema nel computer locale o nei computer remoti. Il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) supporta la classe Del Registro di sistema [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-registry) che contiene dati statici relativi alle dimensioni di un registro.

Il provider del Registro di sistema è un'istanza, una proprietà e un provider di eventi che si interfaccia con il Registro di sistema. Il provider del Registro di sistema è un provider standard con [**l'interfaccia IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) È possibile usare il provider del Registro di sistema per accedere alle chiavi e alle informazioni del Registro di sistema nei sistemi locali e remoti. Per altre informazioni, vedere [Provider del Registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI inserisce [**StdRegProv nello**](/previous-versions/windows/desktop/regprov/stdregprov) spazio dei nomi predefinito \\ radice. Tuttavia, è possibile compilare il file Regevent.mof in altri spazi dei nomi per l'uso da parte di altre applicazioni.

Gli argomenti identificati nella tabella seguente illustrano come usare la [**classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e il provider del Registro di sistema.



| Argomento                                                                                              | Descrizione                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recupero dei dati del Registro di sistema](obtaining-registry-data.md)                                             | È possibile ottenere o modificare i dati del Registro di sistema tramite i metodi della [**classe StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov) che consente di automatizzare le attività del Registro di sistema in locale o in remoto.                    |
| [Modifica dei dati del Registro di sistema](changing-registry-data.md)                                               | È possibile aggiungere o eliminare chiavi e aggiungere o modificare i valori delle voci del Registro di sistema nelle chiavi.                                                                                                                    |
| [Programmazione con il provider del Registro di sistema](programming-with-the-system-registry-provider.md) | È possibile definire classi personalizzate fornite dal Registro di sistema con i dati.                                                                                                                       |
| [Registrazione per gli eventi del Registro di sistema](registering-for-system-registry-events.md)               | Il provider del Registro di sistema può inviare eventi a un consumer. Per ricevere eventi, è necessario registrare il consumer, creare una query e quindi assicurarsi che il provider invii gli eventi correttamente. |
| [Registrazione del provider del Registro di sistema](registering-the-system-registry-provider.md)           | Il provider del Registro di sistema viene registrato come parte del processo di installazione WMI.                                                                                                                |



 

 

 
