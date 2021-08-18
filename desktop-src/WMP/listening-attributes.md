---
title: Attributi di ascolto
description: Attributi di ascolto
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player, attributi di ascolto
- skin, attributi di ascolto
- informazioni di riferimento per le skin, attributi di ascolto
- attributi di ascolto
- attributi, ascolto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cceb9a8721995c494b5e4366291353376a2569c045e41eb41c1418e2f4d5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996411"
---
# <a name="listening-attributes"></a>Attributi di ascolto

Un attributo di ascolto viene usato per connettere un attributo a un altro in modo che il relativo valore cambi ogni volta che cambia il valore dell'altro attributo.

L'attributo di **ascolto wmpprop:** è il più utile. Se il valore di un attributo viene specificato come **wmpprop:** di un secondo attributo, il primo valore verrà aggiornato automaticamente per riflettere il secondo valore ogni volta che il secondo valore cambia.

**Esempio:**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



In questo modo, il valore di mySlider, indicato dalla posizione del dispositivo di scorrimento, può essere visualizzato anche come numero all'interno di una casella di testo.

Gli altri due attributi di ascolto, **wmpenabled:** e **wmpdisabled:**, possono essere usati per modificare l'attributo abilitato di un controllo a seconda che la relativa funzionalità sia attualmente disponibile nel lettore.  Questi attributi possono restare in ascolto solo dei metodi **dell'oggetto** Controls.

**Esempio:**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Varie**](miscellaneous.md)
</dt> </dl>

 

 




