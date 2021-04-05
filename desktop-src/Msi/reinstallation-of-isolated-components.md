---
description: Durante la reinstallazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstallazione dei componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881473"
---
# <a name="reinstallation-of-isolated-components"></a>Reinstallazione dei componenti isolati

Durante la reinstallazione di un'applicazione Windows Installer esegue le azioni seguenti quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.

## <a name="reinstallation"></a>Reinstallazione

-   Reinstallare i file del componente \_ condivisi nella stessa cartella dell' \_ applicazione Component solo se \_ viene reinstallata anche l'applicazione componente.
-   Non incrementare l'elenco client di componenti \_ condivisi e non incrementare il numero di SharedDLL.
-   Ricreare il file di zero byte con il nome breve del file di chiave dell'applicazione componente \_ . Questo file deve trovarsi nella stessa cartella dell'applicazione componente \_ e avere l'estensione. Locale.
-   Reinstallare tutte le risorse dell'applicazione componente \_ come di consueto.

Se il refcount SharedDLL per il componente \_ condiviso è maggiore di 1 o se altri prodotti rimangono nell'elenco client di componenti \_ condivisi:

-   Non reinstallare alcun file nel percorso condiviso del componente \_ condiviso.

Se il refcount SharedDLL per il componente \_ condiviso è uguale a 1 o se non sono presenti altri client rimanenti del componente \_ condiviso:

-   Reinstallare i file del componente \_ condivisi nel percorso condiviso usando le regole di [controllo delle versioni dei file](file-versioning-rules.md).
-   Elabora tutte le azioni di reinstallazione per il componente \_ condiviso.
-   Se Component \_ Shared è un componente com, registrare il percorso com completo in modo che le sintassi del \[ programma \] di installazione $Component e \[ \# FileKey \] puntino al percorso condiviso del componente \_ condiviso.

 

 



