---
title: Aggiunta di caratteri di copyright ai metafile
description: I caratteri per i simboli di registrazione del copyright e del marchio ( \ 169; o \ 174; ) potrebbero non essere visualizzati correttamente se il metafile non è codificato usando lo schema di codifica UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Aggiunta di caratteri di copyright ai metafile Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865161"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Aggiunta di caratteri di copyright ai metafile

I caratteri per i simboli di registrazione del copyright e del marchio ( © o ® ) potrebbero non essere visualizzati correttamente se il metafile non è codificato usando lo schema di codifica UTF-8. In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è possibile usare gli equivalenti ASCII (c) e (r) all'interno dell'elemento **COPYRIGHT,** come illustrato nel codice seguente.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Se il metafile viene codificato usando UTF-8, i simboli di copyright e marchi verranno visualizzati correttamente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




