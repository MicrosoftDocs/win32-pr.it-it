---
title: UI_PKEY_FontProperties_Size
description: Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ Size.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c013c41290f6e062b03572a9e3cb848752efcb12f1c779348a0253f94d40e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028629"
---
# <a name="ui_pkey_fontproperties_size"></a>UI \_ PKEY \_ FontProperties \_ Size

Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ Size.

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Commenti

Ui \_ PKEY \_ FontProperties \_ Size viene usato da un'applicazione per eseguire query sul valore del **controllo Dimensione carattere.**

I valori validi per questa proprietà sono compresi tra 1 e 9999, inclusi. Se un utente tenta di immettere un valore non  valido, la voce viene rifiutata e il controllo Dimensione carattere ripristina l'ultimo valore valido.

Se un'applicazione tenta di impostare le dimensioni del carattere a livello di codice su un valore non compreso nell'intervallo valido, il framework della barra multifunzione invalida tutte le proprietà del carattere e imposta i controlli del tipo di carattere **(** Dimensione carattere e Carattere **)** su vuoto o sul relativo stato predefinito, se appropriato.

Il valore predefinito è 0.

Il valore 0 specifica che non è selezionata alcuna dimensione di punto singolo (non è selezionato alcun testo o un'esecuzione di testo con dimensioni eterogenee).

Un utente non può impostare il **controllo Dimensione** carattere su 0.

Diverso da 0, i valori validi per ui PKEY FontProperties Size sono compresi tra \_ \_ \_ *MinimumFontSize* e *MaximumFontSize,* come dichiarato nel markup [del controllo font.](windowsribbon-controls-fontcontrol.md)

> [!Note]  
> Il **controllo Dimensione** carattere è impostato su vuoto quando la dimensione del carattere è impostata a livello di codice su 0, ad esempio quando viene evidenziata un'esecuzione di testo con dimensioni eterogenee.

 

Quando è selezionata un'esecuzione di testo con dimensioni eterogenee, l'applicazione deve eseguire una query sui comandi UI [ \_ PKEY \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) per acquisire i comandi **Aumenta** tipo di carattere e **Riduci carattere.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




