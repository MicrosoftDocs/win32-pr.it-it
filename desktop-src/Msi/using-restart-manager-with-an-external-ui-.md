---
description: Windows Installer gli sviluppatori possono preparare il pacchetto di installazione in modo che funzioni con Gestione riavvio attenendosi alle linee guida descritte in uso di Windows Installer con Gestione riavvio.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Uso di gestione riavvio con un'interfaccia utente esterna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226122"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Uso di gestione riavvio con un'interfaccia utente esterna

Windows Installer gli sviluppatori possono preparare il pacchetto di installazione in modo che funzioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md) attenendosi alle linee guida descritte in [uso di Windows Installer con Gestione riavvio](using-windows-installer-with-restart-manager.md).

Specificare il \_ tipo di messaggio RMFILESINUSE di INSTALLLOGMODE quando si chiama la funzione [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) o [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) per abilitare il gestore dell'interfaccia utente esterno. Windows Installer quindi Invia un \_ messaggio RMFILESINUSE di INSTALLMESSAGE per l'uso da parte di gestori dell'interfaccia utente esterni che supportano [Gestione riavvio](../rstmgr/restart-manager-portal.md).

Il gestore dell'interfaccia utente esterno deve gestire le informazioni contenute nei \_ messaggi INSTALLMESSAGE RMFILESINUSE. Se nessuna interfaccia utente registrata o interna gestisce il \_ messaggio RMFILESINUSE di INSTALLMESSAGE, Windows Installer Invia un \_ messaggio filesinus INSTALLMESSAGE per l'uso da parte dei gestori esterni esistenti che supportano i \_ messaggi FilesInUse INSTALLMESSAGE e la finestra di dialogo [filesinus](filesinuse-dialog.md) .

L'interfaccia utente esterna può restituire i valori elencati nella tabella seguente.



| Valore restituito dall'interfaccia utente esterna | Azione eseguita da Windows Installer                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | Il pulsante **OK** è stato premuto dall'utente. Il Windows Installer richiede che [Gestione riavvio](../rstmgr/restart-manager-portal.md) arresti e riavvii le applicazioni che contengono i file attualmente in uso.                                                                                                                                               |
| IDCANCEL                 | È stato premuto il pulsante **Annulla** . Annulla l'installazione.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | È stato premuto il pulsante **Ignora** . Ignorare e continuare l'installazione. Al termine dell'installazione verrà richiesto un riavvio.                                                                                                                                                                                                            |
| IDNO                     | È stato premuto il pulsante **No** . Se il pacchetto contiene una finestra di dialogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) , inviare un messaggio 1610. Per ulteriori informazioni, vedere [Windows Installer messaggi di errore](windows-installer-error-messages.md). Se il pacchetto non dispone di una finestra di dialogo MsiRMFilesInUse, inviare un \_ messaggio FILESINUS INSTALLMESSAGE. |
| IDRETRY                  | È stato premuto il pulsante **Riprova** . Inviare il \_ messaggio FILESINUS INSTALLMESSAGE.                                                                                                                                                                                                                                                                 |
| -1                       | Errore. Terminare l'installazione.                                                                                                                                                                                                                                                                                                                |



 

 

 
