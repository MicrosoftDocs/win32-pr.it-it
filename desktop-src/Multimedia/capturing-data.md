---
title: Acquisizione dei dati
description: Acquisizione dei dati
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence (macro)
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045068"
---
# <a name="capturing-data"></a>Acquisizione dei dati

Nell'esempio seguente viene usata la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) per avviare acquisizione video e la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) per copiare i dati acquisiti dal file di acquisizione al file NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




