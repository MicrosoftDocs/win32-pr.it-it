---
description: Windows Il programma di installazione esegue le azioni seguenti durante la reinstallazione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, Component \_ Shared è una DLL condivisa da Applicazione componente e altri file \_ eseguibili client.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstallazione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c624777647ab9e5023cd6c78d9aaa4d20951563f915afcd800ba60ca3b233174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086011"
---
# <a name="reinstallation-of-isolated-components"></a>Reinstallazione di componenti isolati

Windows Il programma di installazione esegue le azioni seguenti durante la reinstallazione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, Component \_ Shared è una DLL condivisa da Applicazione componente e altri file \_ eseguibili client.

## <a name="reinstallation"></a>Reinstallazione

-   Reinstallare i file di Componente condiviso nella stessa cartella dell'applicazione componente solo se viene reinstallata anche \_ \_ \_ l'applicazione componente.
-   Non incrementare l'elenco client di Component \_ Shared e non incrementare il conteggio SharedDLL.
-   Ricreare il file a zero byte con il nome breve del file di chiave dell'applicazione \_ componente. Questo file deve trovarsi nella stessa cartella dell'applicazione \_ componente e avere l'estensione . Locale.
-   Reinstallare tutte le risorse di Applicazione \_ componente come di consueto.

Se il conteggio SharedDLL per Component Shared è maggiore di 1 o se altri prodotti rimangono nell'elenco \_ client di Component \_ Shared:

-   Non reinstallare alcun file nel percorso condiviso del componente \_ condiviso.

Se il conteggio SharedDLL per Component Shared è uguale a 1 o se non sono presenti \_ altri client rimanenti di Component \_ Shared:

-   Reinstallare i file del componente \_ condiviso nel percorso condiviso usando le regole di controllo delle versioni dei [file](file-versioning-rules.md).
-   Elaborare tutte le azioni di reinstallazione per Componente \_ condiviso.
-   Se Component Shared è un componente COM, registrare il percorso COM completo in modo che la sintassi del programma di installazione $Component e FileKey punti al percorso condiviso \_ \[ di Component \] \[ \# \] \_ Shared.

 

 



