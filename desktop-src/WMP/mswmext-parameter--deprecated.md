---
title: Parametro MSWMExt (deprecato)
description: Parametro MSWMExt (deprecato)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Metafile multimediali, parametro MSWMExt
- metafile, parametro MSWMExt
- Parametro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ec80530f95d4429769758488e5a2b24b0268c57255248c7685a0d00125aa130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574598"
---
# <a name="mswmext-parameter-deprecated"></a>Parametro MSWMExt (deprecato)

Il *parametro MSWMExt* indica a un programma client il formato di un file a cui si fa riferimento.

**Sintassi**


```XML

URL?MSWMExt=.
ext
```



**Codice di esempio**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Commenti

I programmi client talvolta usano un'estensione di file o un tipo MIME per determinare se eseguire il rendering di un file multimediale come flusso, eseguire il rendering del file dopo un download completo o rifiutare il rendering del file. Se un programma client non è in grado di determinare come trattare un file multimediale in base all'estensione o al tipo MIME, può determinare come trattare il file controllando il *parametro MSWMExt.* Ad esempio, il client può considerare il file come se avesse un'estensione uguale al valore del *parametro MSWMExt.* Per altre informazioni sui tipi MIME e sulle estensioni di file, vedere [Estensioni di file](file-name-extensions.md). Per altre informazioni sul *parametro MSWMExt,* vedere [l'articolo](https://support.microsoft.com/kb/236895) 236895 nel Microsoft Knowledge Base.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Versioni precedenti di Windows metafile multimediali (deprecati)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




