---
description: Alcuni valori utilizzati con i moduli merge configurabili richiedono una gestione del testo speciale.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato speciale CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226858"
---
# <a name="cmsm-special-format"></a>Formato speciale CMSM

Alcuni valori utilizzati con i moduli merge configurabili richiedono una gestione del testo speciale. Una stringa di testo descritta come nel formato speciale "CMSM" considera il punto e virgola (;) e uguale a (=) caratteri come caratteri riservati utilizzati dallo strumento di merge client o Mergemod.dll.

Il formato speciale CMSM è attualmente usato nei percorsi seguenti:

-   Colonna di riga della [tabella ModuleSubstitution](modulesubstitution-table.md).
-   Colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).
-   La colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando bit è il valore nella colonna Format.
-   La colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando Text è il valore nella colonna Format e enum è il valore nella colonna Type.
-   La colonna DefaultValue della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando Key è il valore nella colonna Format.
-   Elementi configurabili nel formato chiave utilizzato dal [**Metodo ProvideTextData**](configuremodule-providetextdata.md).

Per immettere punti e virgola letterali o caratteri uguali in un valore in formato speciale CMSM, anteporre al carattere una barra rovesciata (' \\ '). Una barra rovesciata letterale può essere rappresentata da due barre rovesciate. Un singolo carattere preceduto da una singola barra rovesciata viene convertito nel carattere singolo, anche se non è necessario l'escape del carattere.

Se un carattere punto e virgola o uguale non è preceduto da una barra rovesciata, ma non ha un comportamento definito nel contesto del valore, la stringa risultante non è definita. La colonna DefaultValue della tabella ModuleConfiguration, ad esempio, è in formato speciale CMSM per tutti gli elementi chiave, perché il carattere punto e virgola è il delimitatore di colonna. Sebbene il carattere uguale non abbia un significato speciale in questa stringa, i caratteri letterali uguali devono comunque essere preceduti da un carattere di escape in questa stringa.

 

 



