---
description: Prima che il motore di configurazione della sicurezza possa chiamare il motore degli allegati per elaborare attività specifiche del servizio, è necessario installare il motore degli allegati e registrarlo con il motore di configurazione della sicurezza.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrazione di un motore degli allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d3d13bab6c26254295734344011a9f56457b8fac28c913178c7515cc147fb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893700"
---
# <a name="registering-an-attachment-engine"></a>Registrazione di un motore degli allegati

Prima che il motore di configurazione della sicurezza possa chiamare il motore degli allegati per elaborare attività specifiche del servizio, è necessario installare il motore degli allegati e registrarlo con il motore di configurazione della sicurezza.

**Per installare e registrare la DLL del motore degli allegati**

1.  Copiare la DLL del motore degli allegati in una directory del sistema. La directory preferita è %windir% \\ secedit \\ attachments. Se questa directory non esiste, è necessario crearla.
2.  Creare una chiave del Registro di sistema nel nodo seguente. Il *nome del servizio* è il nome registrato per l'allegato e deve essere lo stesso nome del servizio usato in Gestione controllo servizi, un modulo che gestisce l'arresto e l'avvio dei servizi. Anche il nome deve essere univoco, in modo che non sia in conflitto con i nomi di altri allegati.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Creare il valore stringa seguente nella nuova chiave del Registro di sistema. *attachment engine path* è il percorso completo del modulo del motore degli allegati.<dl> <dd>**ServiceAttachmentPath**  =  *percorso del motore degli allegati*<dl> <dt>

Tipo di dati
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



