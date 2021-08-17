---
title: Errori di backup in Active Directory Domain Services
description: Questo argomento elenca i valori restituiti degli errori di backup per le funzioni in Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Errori di backup di Active Directory
- Dominio di Active Directory errori di backup del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5038b1d3a7a1f24c2e3b8dbf137aa2722073650b878e1d6a1dfdec8cac399a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024138"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Errori di backup in Active Directory Domain Services

Questo argomento elenca i valori restituiti degli errori di backup per le funzioni in Active Directory Domain Services.



| Valore                                      | Descrizione                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | La funzione non è implementata.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Il parametro non è valido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | An internal error occurred.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | L'handle non è valido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | Il processo di ripristino è in corso.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | Il file specificato è aperto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | I destinatari non sono validi. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Impossibile eseguire il backup. Non è stata rilevata una connessione al server di backup specificato o il servizio di cui si sta tentando di eseguire il backup non è in esecuzione.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Esiste una mappa di ripristino per il componente specificato. Quando si esegue un ripristino completo, è possibile specificare una mappa di ripristino.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Un'altra applicazione ha modificato il Windows NT/Windows 2000 del servizio directory specificato in modo che i backup successivi non riescano. Per risolvere il problema, eseguire un backup completo.<br/> |
| **hrLogFileNotFound**<br/>           | Impossibile eseguire un backup incrementale perché non è stato trovato Windows NT/Windows file di log del database del servizio directory 2000.<br/>                                        |
| **hrCircularLogging**<br/>           | Il Windows NT/Windows servizio directory di 2000 specificato è configurato per l'uso di log di database circolari. Non è possibile eseguire il backup incrementale. Eseguire un backup completo.<br/>       |
| **hrNoFullRestore**<br/>             | I database non sono stati ripristinati in questo computer. Non è possibile ripristinare un backup incrementale finché non viene ripristinato un backup completo.<br/>                                            |
| **hrCommunicationError**<br/>        | Si è verificato un errore di comunicazione durante il tentativo di eseguire un backup locale.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | È necessario eseguire un backup completo prima di poter eseguire un backup incrementale.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Token di scadenza mancante. Impossibile eseguire il ripristino senza i dati di scadenza.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | Il token di scadenza è in un formato non riconoscibile.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | Il contenuto di DS nel backup non è aggiornato. Eseguire il ripristino con una copia recente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Vedere anche

[Success](success.md), [System Errors in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), Directory Manager [Errors](directory-manager-errors.md), Logging and Recovery Errors in Functions [in Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), Return Values for Functions [in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





