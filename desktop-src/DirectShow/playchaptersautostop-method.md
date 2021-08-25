---
description: Il metodo PlayChaptersAutoStop avvia la riproduzione in corrispondenza del capitolo specificato nel titolo specificato e per il numero di capitoli specificati.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Metodo PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c518496f81f4ca4e662bf8dbc821f2378cd38d27c7546356144910c0c5ba72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830741"
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

Specifica il titolo come valore Integer.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Specifica il capitolo iniziale come valore Integer.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Specifica il numero di capitoli da riprodurre come valore Integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando viene riprodotto l'ultimo capitolo, questo metodo determina l'invio all'applicazione di una notifica dell'evento [**\_ EC DVD CHAPTER \_ \_ AUTOSTOP.**](ec-dvd-chapter-autostop.md)

 

 



