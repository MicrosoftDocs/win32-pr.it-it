---
title: Creazione di dispositivi di scorrimento personalizzati
description: Creazione di dispositivi di scorrimento personalizzati
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- creazione di interfacce, dispositivi di scorrimento
- Interfacce di Media Player Windows, dispositivi di scorrimento
- interfacce, dispositivi di scorrimento
- dispositivi di scorrimento nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515913"
---
# <a name="creating-custom-sliders"></a>Creazione di dispositivi di scorrimento personalizzati

È possibile creare dispositivi di scorrimento personalizzati in qualsiasi forma desiderata. Per questo esempio viene scelta una semplice striscia, ma la forma effettiva può essere qualsiasi elemento. Ecco il codice per l'elemento **CUSTOMSLIDER** :


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



In questo modo viene impostato un valore iniziale per il dispositivo di scorrimento. Vengono introdotte due nuove bitmap. Una è la bitmap in scala di grigi (slider.bmp) che definisce i valori che verranno usati quando si fa clic su di esso e l'altro (slider.bmp) che determina quale immagine verrà visualizzata quando si fa clic su una particolare parte della scala di grigi.

Il valore iniziale viene determinato ascoltando il volume con wmpprop e quindi il volume può essere modificato quando l'utente fa clic su una parte del dispositivo di scorrimento che attiva una modifica nel valore.

Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




