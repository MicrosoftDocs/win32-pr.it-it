---
description: Funzioni usate nella gestione delle directory.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funzioni di gestione della directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2042b7fc4cc7f6af64c3c0eba0938b3f5d78e7b551981e1cc820b38000b1d745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150439"
---
# <a name="directory-management-functions"></a>Funzioni di gestione della directory

Nella gestione delle directory vengono usate le funzioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                      | Descrizione                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | Crea una nuova directory.<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | Crea una nuova directory con gli attributi di una directory modello specificata.<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | Crea una nuova directory come operazione transazione, con gli attributi di una directory modello specificata.<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | Arresta il monitoraggio dell'handle di notifica delle modifiche.<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | Crea un handle di notifica delle modifiche e configura le condizioni iniziali del filtro di notifica delle modifiche.<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | Richiede che il sistema operativo segnali una gestione delle notifiche di modifica la volta successiva che rileva una modifica appropriata.<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | Recupera la directory corrente per il processo corrente.<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | Recupera informazioni che descrivono le modifiche all'interno della directory specificata, che possono includere informazioni estese se viene specificato tale tipo di informazioni.<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | Recupera informazioni che descrivono le modifiche all'interno della directory specificata.<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | Elimina una directory vuota esistente.<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | Elimina una directory vuota esistente come operazione transazione.<br/>                                                                                                 |
| [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | Modifica la directory corrente per il processo corrente.<br/>                                                                                                         |



 

 

 




