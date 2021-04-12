---
title: Bordi per Windows Media Player (deprecato)
description: Bordi per Windows Media Player (deprecato)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Media Player di Windows, bordi
- Interfacce di Media Player Windows, bordi
- interfacce, bordi
- bordi, rispetto alle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329884"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordi per Windows Media Player (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Un bordo è simile a un oggetto Skin, ma invece di sostituire l'interfaccia utente per la modalità Compact di Windows Media Player, un bordo è incorporato nel riquadro Now Playing del Media Player Windows in modalità completa.

Utilizzando un pacchetto di download di Windows Media, è possibile includere contenuto con un bordo, aprendo il percorso alle applicazioni multimediali.

Nella directory degli esempi di questo SDK è incluso un pacchetto di download di esempio Windows Media che include un bordo e contenuto incorporato.

## <a name="creating-a-border"></a>Creazione di un bordo

Un bordo viene creato allo stesso modo di un'interfaccia. L'unica differenza è che l'interfaccia è incorporata all'interno del riquadro **Now Play** . Ciò significa che le dimensioni dell'interfaccia non possono essere calcolate e che tutti gli elementi dell'interfaccia devono essere relativi. Se l'utente ridimensiona Windows Media Player, le parti del bordo potrebbero essere ritagliate e non visualizzate.

## <a name="loading-a-border"></a>Caricamento di un bordo

Quando viene caricato un metafile di Windows Media che usa l'elemento **Skin** , viene caricato un bordo. L'attributo **href** dell'elemento **Skin** deve fare riferimento a un'interfaccia. Un tipico elemento **Skin** avrà un aspetto simile al seguente:


```C++
<SKIN HREF="myborder.wmz">

```



Per ulteriori informazioni, vedere [elemento Skin (deprecato)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Inclusione di contenuto con un bordo

È possibile includere contenuto con un bordo utilizzando un file di download di Windows Media (con estensione di file WMD). A tale scopo, seguire questa procedura:

1.  Creare il bordo. Prestare attenzione a crearlo in modo tale che il ridimensionamento non rovini la composizione del bordo. Ad esempio, non includere un file in background; rendere trasparente lo sfondo in modo da consentire l'esecuzione di una visualizzazione sottostante.
2.  Comprimere il contenuto dell'interfaccia (file di immagine, file JScript e definizione di interfaccia personalizzata) in un file con estensione WMZ.
3.  Creare un metafile di Windows Media (con estensione asx) che fa riferimento al file di bordo compresso (con estensione WMZ). Il metafile può includere le informazioni sulla playlist con metadati per l'arte e gli URL per contenuto specifico.
4.  Assemblare il contenuto multimediale digitale.
5.  Comprimere il bordo, il metafile e il contenuto in un file e assegnargli un'estensione del nome di file. WMD.

## <a name="using-a-border"></a>Uso di un bordo

Dopo aver creato il file di download di Windows Media, è sufficiente fare doppio clic su di esso. Il file verrà scaricato nel computer dell'utente. I file all'interno del pacchetto verranno decompressi, la playlist verrà aggiunta alle playlist, il bordo verrà visualizzato nel riquadro **ora riproduzione** del Media Player di Windows in modalità completa e il primo elemento della nuova playlist inizierà a essere riprodotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle interfacce**](about-skins.md)
</dt> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Pacchetti di download di Windows Media (deprecato)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




