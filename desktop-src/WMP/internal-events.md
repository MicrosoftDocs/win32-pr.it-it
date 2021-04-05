---
title: Eventi interni
description: Eventi interni
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player Skin, eventi interni
- interfacce, eventi interni
- eventi, interni
- scrittura di codice per interfacce, eventi interni
- eventi interni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955254"
---
# <a name="internal-events"></a>Eventi interni

È possibile rilevare le modifiche apportate in Windows Media Player o modifiche nell'interfaccia personalizzata. Queste modifiche possono essere apportate alle proprietà o ai metodi dell'oggetto Media Player di Windows, alle modifiche degli attributi di interfaccia e così via.

## <a name="windows-media-player-property-changes"></a>Modifiche alle proprietà di Windows Media Player

È possibile elaborare le modifiche in Windows Media Player usando il listener wmpprop. È necessario configurare il listener come valore di un attributo. Inserire il valore tra virgolette doppie e iniziare con la parola "wmpprop" seguita da due punti. Si includerà quindi la proprietà che si vuole ascoltare. Quando la proprietà viene modificata, anche il valore dell'attributo viene modificato. Ad esempio, per modificare il valore di un elemento Slider ogni volta che viene modificato il valore dell'attributo **currentPosition** , digitare quanto segue:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** Non usare wmpprop nei metodi Media Player di Windows. Potrebbero verificarsi risultati imprevisti.

## <a name="windows-media-player-method-changes"></a>Modifiche al metodo Windows Media Player

È possibile far rispondere la propria interfaccia alla disponibilità dei metodi in Windows Media Player usando wmpenabled e wmpdisabled. Questi vengono usati in modo analogo al listener wmpprop, ad eccezione del fatto che è possibile usarli solo su metodi dell'oggetto **controllo** supportati dal metodo **disavailable** .

Ad esempio, è possibile abilitare un pulsante solo quando il metodo **Play** è abilitato, usando un codice simile al seguente:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** Non usare wmpenabled o wmpdisabled nelle proprietà Media Player di Windows. Potrebbero verificarsi risultati imprevisti.

## <a name="skin-attribute-changes"></a>Modifiche all'attributo Skin

È possibile rispondere alle modifiche negli attributi dell'interfaccia utente in uno dei due modi seguenti, usando wmpprop o l'evento **\_ OnChange** .

È possibile usare wmpprop per restare in ascolto delle modifiche nell'interfaccia personalizzata. Ad esempio, per visualizzare il valore del dispositivo di scorrimento in una casella di testo, è possibile digitare quanto segue:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



È possibile utilizzare l'evento **\_ OnChange** per elaborare gli eventi all'interno di un elemento. È necessario alleghi il nome dell'attributo di cui si vuole tenere traccia per la **\_ modifica**. Se ad esempio si desidera tenere traccia del valore di una casella di testo, digitare:


```C++
value_onchange

```



Si assegnerà quindi una stringa JScript che si desidera eseguire quando cambia il valore. Ad esempio, per rispondere a una modifica nel valore di una casella di testo che può essere usata per regolare il volume di Media Player di Windows, digitare quanto segue all'interno dell'elemento di **testo** come attributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




