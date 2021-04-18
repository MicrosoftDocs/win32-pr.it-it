---
title: File segnaposto
description: File segnaposto
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300637"
---
# <a name="placeholder-files"></a>File segnaposto

## <a name="platform"></a>Piattaforma

**Client-** Windows 8.1  
**Server-** Windows Server 2012 R2  

## <a name="description"></a>Descrizione

I file segnaposto consentono agli utenti di visualizzare e gestire i file di Microsoft OneDrive indipendentemente dalla connettività. I file segnaposto rappresentano lo spazio dei nomi OneDrive, anche quando i file non sono memorizzati nella cache locale. Contengono i metadati dei file e le immagini di anteprima delle foto.

## <a name="manifestation"></a>Manifestazione

Per gli utenti e gli sviluppatori finali, i file segnaposto sembrano comportarsi quasi come i file locali.

Se l'app usa la finestra di dialogo file comune per enumerare la file system, l'app non verrà interessata. Quando l'utente tenta di aprire il file dalla finestra di dialogo/file comune, il contenuto del file verrà scaricato e verrà passato all'app.

Se l'app accede direttamente al file system, è possibile che l'app sfrutti i file segnaposto usando le linee guida riportate di seguito.

## <a name="solution"></a>Soluzione

-   I segnaposto sono nascosti per convenzione in base agli attributi
-   Identificare i segnaposto usando reparse Tag ID i/o \_ \_ file di tag \_ \_ segnaposto

Usare il modello di dati della Shell per un comportamento uniforme:

-   Usare SHCreateItemFromParsingName () per creare un elemento della shell
-   Eseguire l'associazione al flusso usando IShellItem:: BindToHandler ( \_ flusso BHID)
-   Gestore proprietà utente per l'accesso alle proprietà (IShellItem2:: GetPropertyHandler)
-   Thumbnailhandler della shell utente per ottenere le immagini di anteprima per i segnaposto
-   Specificare SupportedProtocols: recupera = nell' \* implementazione del verbo se il verbo viene associato al flusso tramite BindToHandler


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



 

 




