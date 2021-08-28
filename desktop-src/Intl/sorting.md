---
description: Per NLS, ordinamento (noto anche come \# &0034; regole di confronto&\# 0034;) è la disposizione delle stringhe.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordinamento (internazionalizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130211"
---
# <a name="sorting"></a>Ordinamento

Per NLS, l'ordinamento (noto anche come "regole di confronto") è la disposizione delle stringhe. Esistono due tipi di ordinamento:

-   Ordinamento linguistico. Dispone le stringhe con caratteristiche linguistiche simili in gruppi (in base all'ordinamento).
-   Ordinamento ordinale (non linguistico). Dispone le stringhe in una sequenza ordinata.

L'ordinamento usa le funzioni di confronto tra stringhe NLS, ad esempio [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o le funzioni API "wrapper", ad esempio [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), che chiamano internamente le funzioni di confronto tra stringhe NLS.

Per informazioni dettagliate sull'implementazione dell'ordinamento nelle applicazioni, vedere [Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).

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

 

 
