---
title: Analisi delle eccezioni
description: L'API server HTTP fornisce le chiavi del registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analisi delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955578"
---
# <a name="parsing-exceptions"></a>Analisi delle eccezioni

L'API server HTTP fornisce le chiavi del registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti. Queste eccezioni non sono abilitate per impostazione predefinita e devono essere abilitate solo per caso, quando il server riscontra problemi di compatibilità con i client HTTP. Questi valori vengono creati nel seguente percorso del registro di sistema:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

Nella tabella seguente sono elencate le chiavi del registro di sistema fornite per supportare le eccezioni elencate. Per abilitare un'eccezione, impostare il valore di chiave corrispondente su 1 e riavviare il servizio HTTP.



| Nome della chiave                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Consente al parser HTTP di accettare i nomi di intestazione con caratteri separatori, ad esempio '?'.                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Consente al parser HTTP di accettare i valori di intestazione con caratteri di controllo non elaborati (senza escape).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Consente al parser HTTP di accettare verbi o metodi HTTP minuscoli come "Get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Consente al parser HTTP di accettare i caratteri di controllo in absPath e le stringhe di query dell'URL. Nel caso di un URL assoluto, i caratteri di controllo non saranno consentiti nel nome host. Tutte le versioni degli URL, ovvero UTF8, DBCS e ANSI, consentiranno caratteri di controllo. Verranno consentiti tutti i caratteri di controllo ASCII tranne NUL (0x00), LF (0x0A), CR (0x0D) e la scheda orizzontale (0x09). |



 

 

 




