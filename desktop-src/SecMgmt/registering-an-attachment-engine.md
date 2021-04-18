---
description: Prima che il motore di configurazione della sicurezza possa chiamare il motore dell'allegato per elaborare le attività specifiche del servizio, è necessario installare il motore di allegati e registrarlo con il motore di configurazione della sicurezza.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrazione di un motore di allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306426"
---
# <a name="registering-an-attachment-engine"></a>Registrazione di un motore di allegati

Prima che il motore di configurazione della sicurezza possa chiamare il motore dell'allegato per elaborare le attività specifiche del servizio, è necessario installare il motore di allegati e registrarlo con il motore di configurazione della sicurezza.

**Per installare e registrare la DLL del motore allegati**

1.  Copiare la DLL del motore degli allegati in una directory del sistema. La directory preferita è% windir% \\ secedit \\ Attachments. Se questa directory non esiste, è necessario crearla.
2.  Creare una chiave del registro di sistema nel nodo seguente. Il nome del *servizio* è il nome registrato per l'allegato e deve essere lo stesso nome di servizio utilizzato in Gestione controllo servizi, un modulo che gestisce l'arresto e l'avvio dei servizi. Il nome deve essere univoco, pertanto non è in conflitto con i nomi degli altri allegati.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Creare il seguente valore stringa nella nuova chiave del registro di sistema. *percorso motore allegato* è il percorso completo del modulo del motore di collegamento.<dl> <dd>**ServiceAttachmentPath**  =  *percorso motore allegati*<dl> <dt>

Tipo di dati
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



