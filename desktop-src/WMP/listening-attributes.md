---
title: Attributi di ascolto
description: Attributi di ascolto
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Interfacce di Media Player Windows, attributi in ascolto
- interfacce, attributi di ascolto
- riferimento per le interfacce, gli attributi di ascolto
- attributi di ascolto
- attributi, ascolto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515676"
---
# <a name="listening-attributes"></a>Attributi di ascolto

Un attributo in ascolto viene usato per connettere un attributo a un altro, in modo che il valore venga modificato ogni volta che il valore dell'altro attributo viene modificato.

L'attributo listening **wmpprop:** è il più utile. Se il valore di un attributo viene specificato come **wmpprop:** di un secondo attributo, il primo valore verrà aggiornato automaticamente in modo da riflettere il secondo valore ogni volta che viene modificato il secondo valore.

**Esempio:**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



In questo modo, il valore di caslider, illustrato dalla posizione del controllo dispositivo di scorrimento, può essere visualizzato anche come numero in una casella di testo.

Gli altri due attributi di ascolto, **wmpenabled:** e **wmpdisabled:**, possono essere usati per modificare l'attributo **Enabled** di un controllo a seconda che la funzionalità sia attualmente disponibile nel lettore. Questi attributi possono restare in ascolto solo dei metodi dell'oggetto **Controls** .

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

 

 




