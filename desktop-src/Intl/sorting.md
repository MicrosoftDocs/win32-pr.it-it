---
description: Per NLS, ordinamento (noto anche come &\# 0034; collation&\# 0034;) è la disposizione delle stringhe.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordinamento (internazionalizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234049"
---
# <a name="sorting"></a>Ordinamento

Per NLS, l'ordinamento (noto anche come "regole di confronto") è la disposizione delle stringhe. Esistono due tipi di ordinamento:

-   Ordinamento linguistico. Dispone le stringhe con caratteristiche linguistiche simili in gruppi (per ordinamento).
-   Ordinamento ordinale (non linguistico). Dispone le stringhe in una sequenza ordinata.

L'ordinamento usa le funzioni di confronto delle stringhe NLS, ad esempio [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), o le funzioni API "wrapper", ad esempio [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), che chiamano internamente le funzioni di confronto delle stringhe NLS.

Per informazioni dettagliate sull'implementazione dell'ordinamento nelle applicazioni, vedere [gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
