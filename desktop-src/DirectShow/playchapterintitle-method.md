---
description: Il metodo PlayChapterInTitle riproduce il capitolo specificato nel titolo specificato.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Metodo PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875905"
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

Specifica il titolo come valore intero.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Specifica il capitolo come valore intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo avvia la riproduzione nel capitolo specificato e continua la riproduzione a tempo indefinito. Per riprodurre solo un determinato capitolo, usare [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

 

 



