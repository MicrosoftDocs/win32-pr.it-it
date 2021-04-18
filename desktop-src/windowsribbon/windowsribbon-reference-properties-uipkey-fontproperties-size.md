---
title: UI_PKEY_FontProperties_Size
description: Identifica la proprietà della dimensione FontProperties dell'interfaccia utente \_ pkey \_ \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297767"
---
# <a name="ui_pkey_fontproperties_size"></a>\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_

Identifica la proprietà della dimensione FontProperties dell'interfaccia utente \_ pkey \_ \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ dimensioni viene utilizzata da un'applicazione per eseguire una query sul valore del controllo **dimensioni carattere** .

I valori validi per questa proprietà sono compresi tra 1 e 9999 inclusi. Se un utente tenta di immettere un valore non valido, la voce viene rifiutata e il controllo della **dimensione del carattere** viene ripristinato all'ultimo valore valido.

Se un'applicazione tenta di impostare le dimensioni del carattere a livello di codice su un valore non compreso nell'intervallo valido, il Framework della barra multifunzione invalida tutte le proprietà del tipo di carattere e imposta i controlli del tipo di carattere (**dimensione** del carattere e **tipo di carattere**) su blank o sullo stato predefinito, laddove appropriato.

Il valore predefinito è 0.

Il valore 0 indica che non è selezionata alcuna dimensione a punto singolo (nessun testo o un'esecuzione di testo di dimensioni eterogenee).

Un utente non può impostare il controllo della **dimensione del carattere** su 0.

Diverso da 0, i valori validi per \_ l'interfaccia utente pkey \_ FontProperties \_ dimensioni variano tra *MinimumFontSize* e *MaximumFontSize* come dichiarato nel markup del controllo del [tipo di carattere](windowsribbon-controls-fontcontrol.md) .

> [!Note]  
> Il controllo **dimensioni carattere** è impostato su blank quando la dimensione del carattere è impostata a livello di codice su 0, ad esempio quando viene evidenziata un'esecuzione di testo di dimensioni eterogenee.

 

Quando viene selezionata un'esecuzione di testo di dimensioni eterogenee, l'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) per acquisire i comandi di **aumento** dei tipi di carattere e **compatta** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




