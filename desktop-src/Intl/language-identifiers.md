---
description: Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la lingua in un paese o in un'area geografica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6245101099b5df5c192af60a977ede88412f95cca8afda9270b7aba6e1c41ad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106981"
---
# <a name="language-identifiers"></a>Identificatori di lingua

Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la [lingua](locales-and-languages.md) in un paese o in un'area geografica. Ogni lingua ha un identificatore di lingua univoco (tipo di dati LANGID), un valore a 16 bit costituito da un identificatore di lingua primaria e un identificatore di sottolingua. Per informazioni dettagliate su identificatori di lingua, vedere Costanti e stringhe degli [identificatori di lingua](language-identifier-constants-and-strings.md).

Un identificatore di lingua viene costruito usando la macro [**MAKELANGID.**](/windows/desktop/api/Winnt/nf-winnt-makelangid) La figura seguente mostra il formato dei bit in un identificatore di lingua.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Di seguito sono riportati gli identificatori di lingua predefiniti:

-   IMPOSTAZIONI PREDEFINITE \_ DEL \_ SISTEMA LANG. Lingua predefinita del sistema operativo.
-   IMPOSTAZIONI PREDEFINITE \_ \_ DELL'UTENTE LANG. Lingua dell'utente corrente.

L'applicazione può recuperare gli identificatori di lingua correnti usando le funzioni [interfaccia utente multilingue.](multilingual-user-interface.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Costanti e stringhe dell'identificatore di lingua](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



