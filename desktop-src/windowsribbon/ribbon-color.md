---
title: Personalizzazione dei colori della barra multifunzione
description: Il Framework della barra multifunzione di Windows espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Barra multifunzione di Windows, personalizzazione dei colori
- Barra multifunzione, personalizzazione dei colori
- personalizzazione dei colori della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723822"
---
# <a name="customizing-ribbon-colors"></a>Personalizzazione dei colori della barra multifunzione

Il Framework della barra multifunzione di Windows espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
-   [Specificare i colori della barra multifunzione](#specify-ribbon-colors)
-   [Converti RGB in HSB](#convert-rgb-to-hsb)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Le [chiavi di proprietà del Framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare il colore di diversi elementi dell'interfaccia utente in un'applicazione Ribbon. Queste proprietà consentono al framework della barra multifunzione di supportare la personalizzazione, i requisiti di identità e le specifiche di personalizzazione tra le applicazioni.

| Colore della barra multifunzione                     | Chiave di proprietà del Framework                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colore di sfondo                 | [Interfaccia utente \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Colore di evidenziazione (solo Windows 7) | [Interfaccia utente \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* * * * introdotta in Windows 8 * *: * * [UI \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) non può essere impostata in modo indipendente dall' [interfaccia utente \_ \_ ](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)pkey GlobalBackgroundColor.<br/> <br/>                                                              |
| Colore del testo                       | [Interfaccia utente \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * introdotta in Windows 8 **:** le modifiche apportate al valore predefinito di [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 potrebbero richiedere una modifica all' [interfaccia utente pkey \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) nelle app della barra multifunzione progettate per Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Specificare i colori della barra multifunzione

Il Framework della barra multifunzione usa un modello di colore HSB (Hue, Saturation, Brightness), che differisce dagli spazi colori più comuni di Hue, Saturation, luminosità (HSL) o Hue, Saturation, value (HSV). In particolare, B rappresenta un livello di luminosità o luminosità generale invece della luminosità di un colore specifico.

Per specificare il colore degli elementi dell'interfaccia utente nel framework della barra multifunzione, un'applicazione assegna i valori HSB a ognuna delle proprietà dei colori globali. Questi valori vengono quindi applicati in modo universale a tutti gli elementi della barra multifunzione come richiesto dall'applicazione Ribbon (il Framework non supporta l'assegnazione di valori HSB a singoli elementi e controlli).

Introdotta in Windows 8 * *: * *[UI \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) viene assegnato lo stesso valore di [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

Nella tabella seguente vengono descritti i parametri HSB del Framework della barra multifunzione.



Componente

Descrizione

Valori regolati\*

Tonalità (H)

Il colore del pigmento, o effettivo, viene in genere identificato come valore da un intervallo di Circlular compreso tra 0 e 359 gradi.

da 0 (rosso) a 255 (rosso)

Saturazione/i

La purezza, o saturazione, del colore misurato come percentuale da 0 a 100%.

0 (grigio) a 255 (completamente saturo)

Luminosità (B)

La luminosità complessiva o l'oscurità del colore misurato come percentuale da 0 a 100%.

da 0 (scuro) a 255 (chiaro)

\* L'intervallo originale per ogni valore di parametro viene convertito in un intervallo compreso tra 0 e 255 per il Framework.



 

I valori HSB non identificano colori specifici. Al contrario, la combinazione di valori di proprietà HSB influenza il modo in cui le sfumature di colore nell'intera interfaccia utente vengono regolate in relazione.

Quando si assegnano valori HSB personalizzati all' [interfaccia utente \_ pkey \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) e [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), è consigliabile che questi valori siano di un contrasto sufficientemente elevato per garantire la leggibilità. In particolare, il colore del testo deve essere più scuro della sfumatura più chiara dell'interfaccia utente della barra multifunzione. Se necessario, il framework regola automaticamente il \_ valore HSB pkey GlobalTextColor dell'interfaccia utente \_ per fornire un contrasto sufficiente rispetto a qualsiasi sfumatura o sfumatura di sfondo derivata dall'interfaccia utente \_ pkey \_ GlobalBackgroundColor.

> [!Note]  
> In Windows 7, l' [interfaccia utente \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) può essere impostata indipendentemente dall' [interfaccia utente \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

Nell'esempio seguente viene illustrato come specificare un colore personalizzato per l' [interfaccia utente \_ pkey \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)e l' [interfaccia utente \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) proprietà.


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a>Converti RGB in HSB

In questa sezione viene descritta la formula necessaria per la corrispondenza dinamica di un valore HSB del Framework della barra multifunzione, l' [interfaccia utente \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in questo esempio a un colore RGB specifico in fase di esecuzione.

Lo sfondo della riga di tabulazione viene usato come punto di riferimento perché viene sottoposto a rendering come superficie di colore Flat rispetto alla sfumatura di luminosità dello sfondo della barra multifunzione.

È necessaria una conversione preliminare per ottenere un valore HSL intermedio. Questo valore HSL può quindi essere convertito in un valore HSB.

> [!Note]  
> La conversione da RGB a HSL viene eseguita facilmente con la maggior parte del software per la modifica di foto.

 

La conversione di HSL (con ogni componente nell'intervallo compreso tra 0,0 e 1,0) in un'impostazione HSB della barra multifunzione viene eseguita tramite le formule seguenti:

-   <sub>Sfondo</sub> H = Round (255.0 h)
-   <sub>Background</sub> S = Round (255.0 s)
-   B<sub>background</sub> = Round (257.7 + 149,9 ln (L)) se 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida sui colori](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Proprietà del Framework](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





