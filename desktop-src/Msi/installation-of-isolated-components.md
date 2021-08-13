---
description: Windows Il programma di installazione esegue le azioni seguenti durante l'installazione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, Component \_ Shared è una DLL condivisa da Applicazione componente e altri file \_ eseguibili client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installazione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f842f626775dce436abedace96549fd55079c577885aad81492df861cd1a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634126"
---
# <a name="installation-of-isolated-components"></a>Installazione di componenti isolati

Windows Il programma di installazione esegue le azioni seguenti durante l'installazione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, Component \_ Shared è una DLL condivisa da Applicazione componente e altri file \_ eseguibili client.

## <a name="installation"></a>Installazione

-   Copiare i file di Componente condiviso nella stessa cartella dell'applicazione componente solo se è in corso \_ \_ \_ l'installazione di Applicazione componente.
-   Creare un file a zero byte con il nome breve del file di chiave dell'applicazione \_ componente. Individuare questo file nella stessa cartella dell'applicazione \_ componente. Aggiungere l'estensione . LOCAL per questo nome di file.
-   Incrementare il conteggio dei riferimenti SharedDLL se il bit msidbComponentAttributesSharedDllRefCount è impostato nella colonna Attributi della [tabella Component](component-table.md).
-   Registrare l'applicazione componente come client di Component Shared e registrare un percorso di chiave che punta \_ al percorso condiviso di Component \_ \_ Shared.
-   Installare tutte le risorse di Applicazione \_ componente come di consueto.

Se Il componente condiviso o il relativo file di chiave è già installato nel computer, non copiare i file nel \_ percorso condiviso del componente \_ condiviso.

Se Il \_ componente condiviso o il relativo file di chiave non è ancora installato nel computer:

-   Copiare i file di Componente \_ condiviso nel percorso condiviso.
-   Elaborare tutte le azioni di installazione per Componente \_ condiviso.
-   Se Component Shared è un componente COM, registrare il percorso COM completo in modo che la sintassi $Component e FileKey puntino al percorso condiviso \_ \[ di Component \] \[ \# \] \_ Shared.

 

 



