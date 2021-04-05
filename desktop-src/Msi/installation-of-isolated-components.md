---
description: Durante l'installazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installazione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753767"
---
# <a name="installation-of-isolated-components"></a>Installazione di componenti isolati

Durante l'installazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.

## <a name="installation"></a>Installazione

-   Copiare i file di componente \_ condivisi nella stessa cartella dell'applicazione componente \_ solo se è in \_ corso l'installazione dell'applicazione componente.
-   Creare un file di zero byte con il nome breve del file di chiave dell'applicazione componente \_ . Individuare il file nella stessa cartella dell'applicazione componente \_ . Aggiungere l'estensione. LOCALE con questo nome file.
-   Incrementare il refcount SharedDLL se il bit msidbComponentAttributesSharedDllRefCount è impostato nella colonna attributi della [tabella dei componenti](component-table.md).
-   Registrare \_ l'applicazione componente come client del componente \_ condiviso e registrare un percorso della chiave che punta al percorso condiviso del componente \_ condiviso.
-   Installare tutte le risorse dell'applicazione componente \_ come di consueto.

Se il componente \_ condiviso o il relativo file di chiave è già installato nel computer, non copiare i file nel percorso condiviso del componente \_ condiviso.

Se il componente \_ condiviso o il relativo file di chiave non è ancora installato nel computer:

-   Copiare i file del componente \_ condiviso nel percorso condiviso.
-   Elabora tutte le azioni di installazione per il componente \_ condiviso.
-   Se Component \_ Shared è un componente com, registrare il percorso com completo in modo che la sintassi \[ $Component \] e \[ \# FileKey \] puntino al percorso condiviso del componente \_ condiviso.

 

 



