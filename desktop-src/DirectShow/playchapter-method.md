---
description: Il metodo PlayChapter avvia la riproduzione dal capitolo specificato all'interno del titolo corrente.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Metodo PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102341"
---
# <a name="playchapter-method"></a>Metodo PlayChapter

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayChapter` metodo avvia la riproduzione dal capitolo specificato all'interno del titolo corrente.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Specifica l'indice del capitolo nel titolo corrente come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando viene raggiunta la fine del capitolo specificato, questo metodo continua a riprodurre i capitoli successivi, se presenti. Se si vuole riprodurre solo un capitolo specificato, usare [**PlayChaptersAutoStop.**](playchaptersautostop-method.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



