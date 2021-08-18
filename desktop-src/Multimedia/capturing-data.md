---
title: Acquisizione di dati
description: Acquisizione di dati
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- Macro capCaptureSequence
- Macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764ff00dedcc044ed5234f8b647b08eaded35ce191bcb56e05cb35f47450677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941299"
---
# <a name="capturing-data"></a>Acquisizione di dati

L'esempio seguente usa la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) per avviare l'acquisizione video e la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) per copiare i dati acquisiti dal file di acquisizione nel file NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




