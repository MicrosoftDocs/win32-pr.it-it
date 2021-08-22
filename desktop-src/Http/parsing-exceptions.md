---
title: Analisi delle eccezioni
description: L'API server HTTP fornisce chiavi del Registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analisi delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950730"
---
# <a name="parsing-exceptions"></a>Analisi delle eccezioni

L'API server HTTP fornisce chiavi del Registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti. Queste eccezioni non sono abilitate per impostazione predefinita e devono essere abilitate solo caso per caso, quando il server rileva problemi di compatibilità con i client HTTP. Questi valori vengono creati nel percorso del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

Nella tabella seguente sono elencate le chiavi del Registro di sistema fornite per supportare le eccezioni elencate. Per abilitare un'eccezione, impostare il valore della chiave corrispondente su 1 e riavviare il servizio HTTP.



| Nome della chiave                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Consente al parser HTTP di accettare nomi di intestazione con caratteri separatori, ad esempio '?'.                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Consente al parser HTTP di accettare valori di intestazione con caratteri di controllo non elaborati (senza caratteri di escape).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Consente al parser HTTP di accettare metodi/verbi HTTP minuscoli, ad esempio "get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Consente al parser HTTP di accettare caratteri di controllo in abspath e stringhe di query dell'URL. Nel caso di un URL assoluto, i caratteri di controllo non saranno consentiti nel nome host. Tutti i tipi di URL, ad esempio UTF8, DBCS e ANSI, consentiranno i caratteri di controllo. Saranno consentiti tutti i caratteri di controllo ASCII ad eccezione di NUL (0x00), LF (0x0a), CR (0x0d) e Horizontal Tab(0x09). |



 

 

 




