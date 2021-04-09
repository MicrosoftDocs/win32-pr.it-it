---
title: DefaultIcon
description: Fornisce informazioni sulle icone predefinite per le presentazioni iconiche degli oggetti.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047415"
---
# <a name="defaulticon"></a>DefaultIcon

Fornisce informazioni sulle icone predefinite per le presentazioni iconiche degli oggetti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il percorso completo del nome dell'eseguibile dell'applicazione oggetto e l'indice di risorsa dell'icona all'interno del file eseguibile.

**DefaultIcon** identifica l'icona da usare quando, ad esempio, un controllo è ridotto a icona. Questa voce contiene il percorso completo del nome dell'eseguibile dell'applicazione server e l'indice di risorsa dell'icona all'interno del file eseguibile. Le applicazioni possono usare le informazioni fornite da **DefaultIcon** per ottenere un handle di icona con [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 