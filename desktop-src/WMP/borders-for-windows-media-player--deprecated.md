---
title: Bordi per Windows Media Player (deprecato)
description: Bordi per Windows Media Player (deprecato)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player,bordi
- Windows Media Player, bordi
- skin, bordi
- bordi, rispetto alle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32e16fa6e334c5c47f24feadc777b82cee1a12477211bc4e613d22e8fdc4521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123851"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordi per Windows Media Player (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Un bordo è simile a un'interfaccia, ma invece di sostituire l'interfaccia utente per la modalità compatta di Windows Media Player, un bordo viene incorporato nel riquadro In riproduzione dell'interfaccia Windows Media Player.

Usando un pacchetto Windows download multimediale, è possibile includere contenuto con un bordo, aprendo la strada alle applicazioni multimediali.

Un pacchetto Windows di download multimediale di esempio che include un bordo e contenuto incorporato è incluso nella directory degli esempi di questo SDK.

## <a name="creating-a-border"></a>Creazione di un bordo

Un bordo viene creato allo stesso modo di un'interfaccia. L'unica differenza è che l'interfaccia è incorporata nel **riquadro In** riproduzione. Ciò significa che le dimensioni dell'interfaccia non possono essere calcolate e che tutti gli elementi dell'interfaccia devono essere relativi. Se l'utente Windows Media Player, parti del bordo potrebbero essere ritagliate e non visibili.

## <a name="loading-a-border"></a>Caricamento di un bordo

Un bordo viene caricato quando viene caricato Windows metafile multimediale che usa **l'elemento SKIN.** **L'attributo HREF** dell'elemento **SKIN** deve fare riferimento a un'interfaccia. Un tipico **elemento SKIN** sarà simile al seguente:


```C++
<SKIN HREF="myborder.wmz">

```



Per altre informazioni, vedere [Elemento SKIN (deprecato).](skin-element--deprecated.md)

## <a name="including-content-with-a-border"></a>Inclusione di contenuto con un bordo

È possibile includere contenuto con un bordo usando un file di Windows Media Download (con estensione wmd). Seguire questa procedura:

1.  Creare il bordo. È necessario crearlo in modo che il ridimensionamento non intasci la composizione del bordo. Ad esempio, non includere un file in background. rendere trasparente lo sfondo in modo che una visualizzazione possa essere eseguita dietro di esso.
2.  Comprimere il contenuto dell'interfaccia (grafica, JScript e file di definizione dell'interfaccia) in un file con estensione wmz.
3.  Creare un metafile Windows Media (con estensione asx) che faccia riferimento al file con bordo compresso (con estensione wmz). Il metafile può includere informazioni sulle playlist con metadati per la grafica e URL per contenuto specifico.
4.  Assemblare il contenuto multimediale digitale.
5.  Comprimere il bordo, il metafile e il contenuto in un unico file e assegnargli l'estensione wmd.

## <a name="using-a-border"></a>Uso di un bordo

Dopo aver creato il Windows file di download multimediale, è necessario fare doppio clic su di esso. Il file verrà scaricato nel computer dell'utente. I file all'interno del pacchetto verranno decompressi, la playlist verrà aggiunta  alle playlist, il bordo verrà visualizzato nel riquadro In riproduzione del Windows Media Player in modalità completa e inizierà la riproduzione del primo elemento nella nuova playlist.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle skin**](about-skins.md)
</dt> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Windows Pacchetti di download multimediali (deprecati)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




