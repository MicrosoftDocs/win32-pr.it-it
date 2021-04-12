---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330239"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Testo

L'elemento con un ControlType di {0} deve supportare almeno uno di questi modelli: {1} ma questo elemento non

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Il supporto per l'automazione interfaccia utente dell'elemento non è conforme alla specifica di automazione interfaccia utente, perché l'elemento deve supportare almeno uno dei pattern di controllo forniti. Di conseguenza, questo elemento potrebbe non essere esposto correttamente alle tecnologie assistive, che potrebbero avere un notevole effetto sull'esperienza utente.

## <a name="possible-causes"></a>Possibili cause

-   Implementazione di automazione interfaccia utente incompleta.
-   La proprietà ControlType non è impostata correttamente.

## <a name="remarks"></a>Commenti

AccChecker registra questo messaggio di errore per un indicatore di stato indeterminato. È possibile ignorare questo messaggio e/o aggiungerlo all'elenco delle eliminazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




