---
title: Creazione di dispositivi di scorrimento personalizzati
description: Creazione di dispositivi di scorrimento personalizzati
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- creazione di skin, dispositivi di scorrimento
- Windows Media Player, dispositivi di scorrimento
- skin, dispositivi di scorrimento
- dispositivi di scorrimento nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85a789bbd90003b59e1a9b9dcf8fffcf4a126c38138f7a051c24125780f8c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902331"
---
# <a name="creating-custom-sliders"></a>Creazione di dispositivi di scorrimento personalizzati

È possibile creare dispositivi di scorrimento personalizzati in qualsiasi forma. Per questo esempio viene scelta una striscia semplice, ma la forma effettiva può essere qualsiasi elemento. Ecco il codice per **l'elemento CUSTOMSLIDER:**


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



In questo modo viene impostato un valore iniziale per il dispositivo di scorrimento. Vengono introdotte due nuove bitmap. Una è la bitmap in scala di grigi (slider.bmp) che definisce i valori che verranno usati quando si fa clic su e l'altra (slider.bmp) che determina l'immagine da visualizzare quando si fa clic su una particolare parte della scala di grigi.

Il valore iniziale è determinato dall'ascolto del volume con wmpprop e quindi il volume può essere modificato quando l'utente fa clic su una parte del dispositivo di scorrimento che attiva una modifica nel valore.

È possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile nella sezione di esempio dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




