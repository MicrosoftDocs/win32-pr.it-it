---
title: Funzionamento delle proprietà
description: Funzionamento delle proprietà
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player plug-in, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP,proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdefea3fce39b70d20d2f100d36cc4aeb8770bd15cd5cd0bf0978cd08f2259f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339135"
---
# <a name="how-properties-work"></a>Funzionamento delle proprietà

I valori delle proprietà vengono archiviati nelle variabili membro.

Le proprietà sono rese accessibili dalle coppie di metodi. Un metodo fornisce l'implementazione per specificare il valore della proprietà. il nome inizia con put \_ . L'altro metodo fornisce l'implementazione per recuperare il valore della proprietà. il nome inizia con get \_ . La definizione dell'interfaccia si trova in Echo.idl. I prototipi del metodo di proprietà sono in Echo.h. Vengono implementati in Echo.cpp.

Le tre sezioni successive illustrano come modificare i metodi di proprietà esistenti in base alle esigenze e come aggiungere i metodi per una proprietà aggiuntiva.

-   [Variabili per archiviare le proprietà](variables-to-store-properties.md)
-   [Modifica della proprietà Scale](modifying-the-scale-property.md)
-   [Aggiunta della proprietà Wet Mix](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà di esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




