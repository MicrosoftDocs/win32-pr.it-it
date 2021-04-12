---
title: Parametro MSWMExt (deprecato)
description: Parametro MSWMExt (deprecato)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metafile di Windows Media, parametro MSWMExt
- Metafile, parametro MSWMExt
- Parametro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398666"
---
# <a name="mswmext-parameter-deprecated"></a>Parametro MSWMExt (deprecato)

Il parametro *MSWMExt* indica a un programma client il formato di un file a cui si fa riferimento.

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

I programmi client a volte usano un'estensione di file o un tipo MIME per determinare se eseguire il rendering di un file multimediale come flusso, eseguire il rendering del file dopo un download completo o rifiutare il rendering del file. Se un programma client non è in grado di determinare come gestire un file multimediale in base all'estensione del nome di file o al tipo MIME, può determinare come trattare il file esaminando il parametro *MSWMExt* . Ad esempio, il client potrebbe trattare il file come se disponesse di un'estensione uguale al valore del parametro *MSWMExt* . Per ulteriori informazioni sui tipi MIME e sulle estensioni dei nomi di file, vedere [estensioni di file](file-name-extensions.md). Per ulteriori informazioni sul parametro *MSWMExt* , vedere l'articolo [236895](https://support.microsoft.com/kb/236895) della Microsoft Knowledge base.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Versioni precedenti dei file di Windows Media (deprecato)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




