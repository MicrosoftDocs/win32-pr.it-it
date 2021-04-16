---
description: Il metodo PlayChaptersAutoStop avvia la riproduzione nel capitolo specificato nel titolo specificato e per il numero di capitoli specificati.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Metodo PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225380"
---
# <a name="playchaptersautostop-method"></a>Metodo PlayChaptersAutoStop

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayChaptersAutoStop` metodo avvia la riproduzione in corrispondenza del capitolo specificato nel titolo specificato e per il numero di capitoli specificati.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica il titolo come valore intero.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Specifica il capitolo iniziale come valore intero.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Specifica il numero di capitoli da riprodurre come valore intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando l'ultimo capitolo è stato riprodotto, questo metodo fa in modo che un [**\_ capitolo del DVD \_ \_ EC**](ec-dvd-chapter-autostop.md) venga inviato all'applicazione.

 

 



