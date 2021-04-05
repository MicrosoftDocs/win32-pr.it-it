---
title: Funzionamento delle proprietà
description: Funzionamento delle proprietà
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711563"
---
# <a name="how-properties-work"></a>Funzionamento delle proprietà

I valori delle proprietà vengono archiviati in variabili membro.

Le proprietà vengono rese accessibili dalle coppie di metodi. Un metodo fornisce l'implementazione per specificare il valore della proprietà. il nome inizia con put \_ . L'altro metodo fornisce l'implementazione per recuperare il valore della proprietà. il nome inizia con Get \_ . La definizione dell'interfaccia è in Echo. idl. I prototipi dei metodi di proprietà si trovano in Echo. h. Sono implementati in Echo. cpp.

Nelle tre sezioni successive verrà illustrato come modificare i metodi di proprietà esistenti in base alle proprie esigenze e come aggiungere i metodi per una proprietà aggiuntiva.

-   [Variabili per archiviare le proprietà](variables-to-store-properties.md)
-   [Modifica della proprietà scale](modifying-the-scale-property.md)
-   [Aggiunta della proprietà Wet Mix](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà di esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




