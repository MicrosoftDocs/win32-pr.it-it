---
description: Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la lingua in un paese o in un'area geografica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307854"
---
# <a name="language-identifiers"></a>Identificatori di lingua

Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la [lingua](locales-and-languages.md) in un paese o in un'area geografica. Ogni lingua dispone di un identificatore di lingua univoco (tipo di dati LANGID), un valore a 16 bit costituito da un identificatore di lingua principale e un identificatore di lingua. Per informazioni dettagliate sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](language-identifier-constants-and-strings.md).

Un identificatore di lingua viene costruito usando la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) . Nella figura seguente viene illustrato il formato dei bit in un identificatore di lingua.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Gli identificatori di lingua predefiniti sono i seguenti:

-   \_impostazione predefinita del sistema lang \_ . Lingua predefinita del sistema operativo.
-   \_impostazione predefinita dell'utente lang \_ . Lingua dell'utente corrente.

L'applicazione può recuperare gli identificatori di lingua correnti utilizzando le funzioni dell' [interfaccia utente multilingue](multilingual-user-interface.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Costanti e stringhe degli identificatori di lingua](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



