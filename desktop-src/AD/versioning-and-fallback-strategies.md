---
title: Strategie di controllo delle versioni e fallback
description: Quando un'applicazione rileva un aggiornamento parziale usando una delle tecniche precedenti o legge un set di oggetti la cui data di validità non è ancora stata raggiunta, l'applicazione deve gestire correttamente la situazione.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Strategie di controllo delle versioni e fallback AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55226efcd72cec4f6dbe65447a945733dac88a56b976661bcf24564c9b366ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024415"
---
# <a name="versioning-and-fallback-strategies"></a>Strategie di controllo delle versioni e fallback

Quando un'applicazione rileva un aggiornamento parziale usando una delle tecniche precedenti o legge un set di oggetti la cui data di validità non è ancora stata raggiunta, l'applicazione deve gestire correttamente la situazione. Per alcune applicazioni, la risposta corretta è eseguire il "fall back" a una versione precedente degli oggetti in questione. Active Directory Domain Services non forniscono una funzionalità di controllo delle versioni, le applicazioni che vogliono questa funzionalità devono fornirla da sole. Gli approcci al controllo delle versioni includono la memorizzazione nella cache locale dei valori "last known good" e l'archiviazione di più set di oggetti nella directory, ad esempio nei contenitori "old", "current" e "new". Sono possibili molti altri schemi.

Le implementazioni devono fare attenzione per evitare conseguenze impreviste. Una versione precedente degli oggetti deve essere usata solo quando viene rilevato un aggiornamento parziale o i nuovi oggetti non sono ancora "effettivi". Il rollback perché un elemento nell'applicazione "non funziona" potrebbe aggirare la finalità di un amministratore. Ad esempio, due computer che in precedenza potevano comunicare potrebbero non essere in grado di farlo a causa di una modifica dei criteri IPsec (Internet Protocol Security). Se si tratta di un'operazione intenzionale da parte dell'amministratore, i sistemi interessati non devono eseguire il fall back ai criteri che consentivano loro di comunicare, in quanto si tratta di una violazione della sicurezza.

 

 




