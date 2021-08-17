---
title: File segnaposto
description: File segnaposto
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8891fef6c7fc54a66c093507b1831ab7cc6525ea96d685d06cf6fa8d9ded1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452501"
---
# <a name="placeholder-files"></a>File segnaposto

## <a name="platform"></a>Piattaforma

**Client -** Windows 8.1  
**Server -** Windows Server 2012 R2  

## <a name="description"></a>Descrizione

I file segnaposto consentono agli utenti di visualizzare e gestire Microsoft OneDrive file indipendentemente dalla connettività. I file segnaposto rappresentano lo OneDrive spazio dei nomi, anche quando i file non vengono memorizzati nella cache locale. Contengono i metadati dei file e le immagini di anteprima delle foto.

## <a name="manifestation"></a>Manifestazione

Per gli utenti finali e gli sviluppatori, i file segnaposto hanno un aspetto e un comportamento quasi uguali a quello dei file locali.

Se l'app usa la finestra di dialogo file comune per enumerare file system, l'app non verrà influenzata. Quando l'utente tenta di aprire il file dalla comune finestra di dialogo /file, il contenuto del file verrà scaricato e verrà passato all'app.

Se l'app accede direttamente file system, l'app può sfruttare i file segnaposto usando le linee guida seguenti.

## <a name="solution"></a>Soluzione

-   I segnaposto sono nascosti per convenzione in base agli attributi
-   Identificare i segnaposto usando l'ID del tag reparse IO \_ REPARSE \_ TAG FILE \_ \_ PLACEHOLDER

Usare il modello di dati della shell per un comportamento facile:

-   Usare SHCreateItemFromParsingName() per creare un elemento della shell
-   Eseguire l'associazione al flusso usando IShellItem::BindToHandler(flusso \_ DISID)
-   Gestore della proprietà utente per l'accesso alle proprietà (IShellItem2::GetPropertyHandler)
-   Thumbnailhandler della shell utente per ottenere le immagini di anteprima per i segnaposto
-   Specificare SupportedProtocols= nell'implementazione del verbo se il verbo si associa \* al flusso tramite BindToHandler


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




