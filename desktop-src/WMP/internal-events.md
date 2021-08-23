---
title: Eventi interni
description: Eventi interni
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player, eventi interni
- interfaccia, eventi interni
- eventi, interno
- scrittura di codice per le interfaccia, eventi interni
- eventi interni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8859ed86cb4951509d452b24c108e73d4129e474abf1c0bc2f51487e2d42bd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572521"
---
# <a name="internal-events"></a>Eventi interni

È possibile rilevare le modifiche che si verificano Windows Media Player o modifiche nell'interfaccia. Possono trattarsi di modifiche Windows Media Player proprietà o metodi dell'oggetto, modifiche negli attributi dell'interfaccia e così via.

## <a name="windows-media-player-property-changes"></a>Windows Media Player Modifiche alle proprietà

È possibile elaborare le modifiche Windows Media Player usando il listener wmpprop. È necessario configurare il listener come valore di un attributo. Inserire il valore tra virgolette doppie e iniziare con la parola "wmpprop" seguita da due punti. Includere quindi la proprietà su cui si vuole restare in ascolto. Quando la proprietà viene modificata, anche il valore dell'attributo cambia. Ad esempio, per fare in modo che il valore di un elemento dispositivo di scorrimento cambi ogni volta che cambia il valore **dell'attributo currentPosition,** digitare quanto segue:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** Non usare wmpprop nei Windows Media Player seguenti. Possono verificarsi risultati imprevisti.

## <a name="windows-media-player-method-changes"></a>Windows Media Player Modifiche ai metodi

È possibile fare in modo che l'interfaccia risponda alla disponibilità dei metodi Windows Media Player usando wmpenabled e wmpdisabled. Questi vengono usati in modo analogo al listener wmpprop, ad eccezione del fatto che è possibile usarli solo nei metodi dell'oggetto **Control** supportati dal **metodo isAvailable.**

Ad esempio, è possibile abilitare un pulsante solo quando è abilitato il **metodo Play,** usando codice simile al seguente:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** Non usare wmpenabled o wmpdisabled Windows Media Player proprietà. Possono verificarsi risultati imprevisti.

## <a name="skin-attribute-changes"></a>Modifiche degli attributi dell'interfaccia

È possibile rispondere alle modifiche negli attributi dell'interfaccia in uno dei due modi seguenti, usando wmpprop o **\_ l'evento onchange.**

È possibile usare wmpprop per ascoltare le modifiche nell'interfaccia. Ad esempio, per visualizzare il valore Slider in una casella di testo, è possibile digitare quanto segue:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



È possibile usare **\_ l'evento onchange** per elaborare gli eventi all'interno di un elemento. È necessario associare il nome dell'attributo di cui si vuole tenere traccia per **\_ l'onchange.** Ad esempio, se si vuole tenere traccia del valore di una casella di testo, digitare:


```C++
value_onchange

```



È quindi necessario assegnare JScript stringa che si vuole eseguire quando il valore cambia. Ad esempio, per rispondere a una modifica nel valore di una casella di testo che può essere usata per regolare il volume di Windows Media Player, digitare quanto segue all'interno dell'elemento **TEXT** come attributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




