---
title: Errori di backup in Active Directory Domain Services
description: Questo argomento elenca i valori restituiti dall'errore di backup per le funzioni in Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Errori di backup Active Directory
- Errori di backup del servizio Dominio di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9b38ba9f28e47fd95e69a923e953d59fdd4d37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470771"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Errori di backup in Active Directory Domain Services

Questo argomento elenca i valori restituiti dall'errore di backup per le funzioni in Active Directory Domain Services.



| Valore                                      | Descrizione                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | La funzione non è implementata.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Il parametro non è valido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | An internal error occurred.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | Handle non valido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | Il processo di ripristino è in corso.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | Il file specificato è aperto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | I destinatari non sono validi. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Non è possibile eseguire il backup. Non è stata rilevata una connessione al server di backup specificato oppure il servizio di cui si sta tentando di eseguire il backup non è in esecuzione.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Esiste una mappa di ripristino per il componente specificato. Quando si esegue un ripristino completo, è possibile specificare una mappa di ripristino.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Un'altra applicazione ha modificato il database del servizio directory Windows NT/Windows 2000 specificato, in modo che eventuali backup successivi avranno esito negativo. Per risolvere il problema, eseguire un backup completo.<br/> |
| **hrLogFileNotFound**<br/>           | Non è possibile eseguire un backup incrementale perché non è stato trovato un file di log del database del servizio directory Windows NT/Windows 2000 obbligatorio.<br/>                                        |
| **hrCircularLogging**<br/>           | Il componente del servizio directory Windows NT/Windows 2000 specificato è configurato per l'utilizzo di log di database circolari. Non è possibile eseguire il backup incrementale. Eseguire un backup completo.<br/>       |
| **hrNoFullRestore**<br/>             | I database non sono stati ripristinati nel computer. Non è possibile ripristinare un backup incrementale fino a quando non viene ripristinato un backup completo.<br/>                                            |
| **hrCommunicationError**<br/>        | Si è verificato un errore di comunicazione durante il tentativo di eseguire un backup locale.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Prima di poter eseguire un backup incrementale, è necessario eseguire un backup completo.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Il token di scadenza è mancante. Non è possibile eseguire il ripristino senza i dati di scadenza.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | Il formato del token di scadenza non è riconoscibile.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | I contenuti DS nel backup non sono aggiornati. Ripristino con una copia recente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Vedere anche

[Esito positivo](success.md), [errori di sistema in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), errori di [Directory Manager](directory-manager-errors.md), [errori di registrazione e ripristino nelle funzioni di Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [valori restituiti per le funzioni in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





