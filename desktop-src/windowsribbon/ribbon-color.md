---
title: Personalizzazione dei colori della barra multifunzione
description: Il Windows del framework della barra multifunzione espone un set di proprietà di colore che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows Barra multifunzione, personalizzazione dei colori
- Barra multifunzione, personalizzazione dei colori
- personalizzazione dei Windows della barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef83c40d49656c82aabfbf41c4ec5375f7f3f54f063ccf30d917e740f87408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710891"
---
# <a name="customizing-ribbon-colors"></a>Personalizzazione dei colori della barra multifunzione

Il Windows del framework della barra multifunzione espone un set di proprietà di colore che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
-   [Specificare i colori della barra multifunzione](#specify-ribbon-colors)
-   [Convertire RGB in HSB](#convert-rgb-to-hsb)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Le [chiavi delle proprietà del framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare il colore di vari elementi dell'interfaccia utente in un'applicazione barra multifunzione. Queste proprietà consentono al framework della barra multifunzione di supportare la personalizzazione, i requisiti di identità e le specifiche di personalizzazione tra le applicazioni.

| Colore della barra multifunzione                     | Chiave di proprietà del framework                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colore di sfondo                 | [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Colore di evidenziazione (solo Windows 7) | [Interfaccia utente \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)****Introduced in Windows 8**: ** [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Colore del testo                       | [Interfaccia utente \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)****Introdotto in **Windows 8:** le modifiche al valore predefinito di [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 potrebbero richiedere una regolazione dell'interfaccia utente [ \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) nelle app della barra multifunzione progettate per Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Specificare i colori della barra multifunzione

Il framework della barra multifunzione usa un modello di colore Hue, Saturation, Brightness (HSB), che differisce dagli spazi colori più comuni di tonalità, saturazione, luminosità (HSL) o tonalità, saturazione, valore (HSV). In particolare, B rappresenta un livello di luminosità o luminosità complessivo anziché la luminosità di un determinato colore.

Per specificare il colore degli elementi dell'interfaccia utente nel framework della barra multifunzione, un'applicazione assegna valori HSB a ognuna delle proprietà di colore globali. Questi valori vengono quindi applicati universalmente in tutti gli elementi della barra multifunzione come richiesto dall'applicazione barra multifunzione (il framework non supporta l'assegnazione di valori HSB a singoli elementi e controlli).

Introdotto in Windows 8**: **[UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) viene assegnato lo stesso valore di [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

La tabella seguente descrive i parametri HSB del framework della barra multifunzione.



Componente

Descrizione

Valori regolati\*

Tonalità (H)

Il colore rosso, o effettivo, viene in genere identificato come valore compreso tra 0 e 359 gradi in un intervallo circolare compreso tra 0 e 359 gradi.

Da 0 (rosso) a 255 (rosso)

Saturazione (S)

Purezza, o saturazione, del colore misurato come percentuale da 0 a 100%.

Da 0 (grigio) a 255 (completamente saturo)

Luminosità (B)

Luminosità o luminosità complessiva del colore misurata come percentuale da 0 a 100%.

Da 0 (scuro) a 255 (chiaro)

\* L'intervallo originale per ogni valore del parametro viene convertito in un intervallo compreso tra 0 e 255 per il framework.



 

I valori HSB non identificano colori specifici. La combinazione di valori della proprietà HSB influisce invece sul modo in cui le sfumature di colore nell'interfaccia utente vengono regolate l'una rispetto all'altra.

Quando si assegnano valori HSB personalizzati a [UI \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) e [UI \_ PKEY \_ GlobalBackgroundColor,](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)è consigliabile che questi valori siano sufficientemente elevati per garantire la leggibilità. In particolare, il colore del testo deve essere più scuro della sfumatura più chiara dell'interfaccia utente della barra multifunzione. Se necessario, il framework regola automaticamente il valore HSB ui PKEY GlobalTextColor per offrire un contrasto sufficiente rispetto a qualsiasi sfumatura o sfumatura di sfondo derivata da \_ \_ UI \_ PKEY \_ GlobalBackgroundColor.

> [!Note]  
> In Windows 7, [L'interfaccia utente \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) può essere impostata indipendentemente da [UI \_ PKEY \_ GlobalBackgroundColor.](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)

 

L'esempio seguente illustra come specificare un colore personalizzato per le proprietà [UI \_ PKEY \_ GlobalTextColor,](windowsribbon-reference-properties-uipkey-globaltextcolor.md) [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)e [UI \_ PKEY \_ GlobalHighlightColor.](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)


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



## <a name="convert-rgb-to-hsb"></a>Convertire RGB in HSB

Questa sezione descrive la formula necessaria per la corrispondenza dinamica di un valore HSB del framework della barra multifunzione, L'interfaccia utente [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in questo esempio, a un colore RGB specifico in fase di esecuzione.

Lo sfondo della riga della scheda viene usato come punto di riferimento perché viene eseguito il rendering come superficie di colore piana rispetto alla sfumatura di luminosità dello sfondo della barra multifunzione.

Per ottenere un valore HSL intermedio, è necessaria una conversione preliminare. Questo valore HSL può quindi essere convertito in un valore HSB.

> [!Note]  
> La conversione da RGB a HSL è facilmente realizzabile con la maggior parte del software di modifica delle foto.

 

La conversione di HSL (con ogni componente compreso nell'intervallo da 0.0 a 1.0) in un'impostazione HSB della barra multifunzione viene eseguita tramite le formule seguenti:

-   Sfondo<sub>H</sub> = Round(255.0 H)
-   S<sub>background</sub> = Round(255.0 S)
-   Sfondo<sub></sub> B = Round(257,7 + 149,9 ln(L)) se 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per i colori](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Proprietà del framework](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





