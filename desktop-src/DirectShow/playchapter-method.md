---
description: Il metodo PlayChapter avvia la riproduzione dal capitolo specificato all'interno del titolo corrente.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Metodo PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303704"
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

Specifica l'indice del capitolo nel titolo corrente come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando viene raggiunta la fine del capitolo specificato, questo metodo continua a riprodurre i capitoli successivi, se presenti. Se si desidera riprodurre solo un capitolo specificato, utilizzare [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



