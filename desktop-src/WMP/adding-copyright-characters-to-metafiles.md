---
title: Aggiunta di caratteri di copyright a metafile
description: I caratteri per il copyright e i simboli di registrazione dei marchi (\ 169; o \ 174;) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Aggiunta di caratteri di copyright a file di Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333967"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Aggiunta di caratteri di copyright a metafile

I caratteri per il copyright e i simboli di registrazione dei marchi (© o®) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8. In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è possibile usare gli equivalenti ASCII (c) e (r) all'interno dell'elemento **Copyright** , come illustrato nel codice seguente.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Se il metafile è codificato con UTF-8, i simboli del copyright e dei marchi vengono visualizzati correttamente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




