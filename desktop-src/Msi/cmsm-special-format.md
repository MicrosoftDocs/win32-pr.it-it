---
description: Alcuni valori usati con moduli unione configurabili richiedono una gestione speciale del testo.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato speciale CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252141"
---
# <a name="cmsm-special-format"></a>Formato speciale CMSM

Alcuni valori usati con moduli unione configurabili richiedono una gestione speciale del testo. Una stringa di testo descritta come in "Formato speciale CMSM" considera il punto e virgola (;) ed è uguale a (=) come caratteri riservati usati dallo strumento di unione client o Mergemod.dll.

Il formato CMSM Special viene attualmente usato nelle posizioni seguenti:

-   Colonna Row della [tabella ModuleSubstitution](modulesubstitution-table.md).
-   Colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md).
-   Colonna ContextData della tabella [ModuleConfiguration quando](moduleconfiguration-table.md) Bitfield è il valore nella colonna Format.
-   Colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md) quando Text è il valore della colonna Format ed Enum è il valore nella colonna Type.
-   Colonna DefaultValue della tabella [ModuleConfiguration quando](moduleconfiguration-table.md) Chiave è il valore nella colonna Formato.
-   Elementi configurabili nel formato Chiave usato dal [**metodo ProvideTextData**](configuremodule-providetextdata.md).

Per immettere un punto e virgola letterale o caratteri uguali in un valore in formato speciale CMSM, antesci il carattere con una barra rovesciata (' \\ '). Una barra rovesciata letterale può essere rappresentata da due barre rovesciate. Un singolo carattere preceduto da una singola barra rovesciata viene convertito nel singolo carattere, anche se non è necessario eseguire l'escape del carattere.

Se un punto e virgola o un carattere uguale non è preceduto da una barra rovesciata ma non ha un comportamento definito nel contesto del valore, la stringa risultante non è definita. Ad esempio, la colonna DefaultValue della tabella ModuleConfiguration è in formato cmsm speciale per tutti gli elementi Key perché il punto e virgola è il delimitatore di colonna. Anche se il carattere uguale non ha alcun significato speciale in questa stringa, i caratteri letterali uguali devono comunque essere preceduti da caratteri di escape in questa stringa.

 

 



