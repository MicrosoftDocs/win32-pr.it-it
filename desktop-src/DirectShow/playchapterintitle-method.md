---
description: Il metodo PlayChapterInTitle riproduce il capitolo specificato nel titolo specificato.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Metodo PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830871"
---
# <a name="playchapterintitle-method"></a>Metodo PlayChapterInTitle

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayChapterInTitle` metodo riproduce il capitolo specificato nel titolo specificato.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica il titolo come valore Integer.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Specifica il capitolo come valore Integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo avvia la riproduzione in corrispondenza del capitolo specificato e quindi continua la riproduzione per un periodo illimitato. Se si vuole riprodurre solo un capitolo specifico, usare [**PlayChaptersAutoStop.**](playchaptersautostop-method.md)

 

 



