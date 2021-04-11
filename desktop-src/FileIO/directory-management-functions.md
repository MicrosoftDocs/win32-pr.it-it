---
description: Funzioni utilizzate nella gestione delle directory.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funzioni di gestione della directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233161"
---
# <a name="directory-management-functions"></a>Funzioni di gestione della directory

Le funzioni seguenti vengono utilizzate per la gestione delle directory.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                      | Descrizione                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | Crea una nuova directory.<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | Crea una nuova directory con gli attributi di una directory di modello specificata.<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | Crea una nuova directory come operazione transazionale, con gli attributi di una directory di modello specificata.<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | Arresta il monitoraggio dell'handle della notifica di modifica.<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | Crea un handle notifica di modifica e configura le condizioni di filtro della notifica di modifica iniziale.<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | Richiede che il sistema operativo segnali un handle della notifica di modifica alla successiva rilevazione di una modifica appropriata.<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | Recupera la directory corrente per il processo corrente.<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | Recupera le informazioni che descrivono le modifiche all'interno della directory specificata, che possono includere informazioni estese se è specificato il tipo di informazioni.<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | Recupera le informazioni che descrivono le modifiche all'interno della directory specificata.<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | Elimina una directory vuota esistente.<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | Elimina una directory vuota esistente come operazione transazionale.<br/>                                                                                                 |
| [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | Modifica la directory corrente per il processo corrente.<br/>                                                                                                         |



 

 

 




