---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc8e413c12b93ebcb3fcbb9d38e56041bedf4e0b8abb98581d77fae4c275f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071811"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Testo

Questo elemento sembra essere tabbable ma non è nell'ordine di tabulazione.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento attivabile non è accessibile tramite la navigazione da tastiera standard (TAB o MAIUSC+TAB). Ad esempio, l'elemento non è stato contrassegnato come tabulazione o non è stato assegnato un indice di tabulazione. Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione perché:

-   L'elemento non è individuabile.
-   Se l'elemento è figlio di un controllo elenco personalizzato, i segnali che indicano che l'elemento figlio può essere esplorato usando la freccia o i tasti Di pagina potrebbero mancare.

## <a name="possible-causes"></a>Possibili cause

-   Il ruolo MSAA dell'elemento o del relativo elemento padre non è impostato correttamente. Ad esempio, se tutti gli elementi dell'elenco in un controllo visualizzazione elenco non vengono esposti tramite MSAA come ROLE SYSTEM LISTITEM, la verifica non riesce perché gli elementi dell'elenco non sono accessibili tramite \_ \_ tab.
-   L'elemento o il relativo elemento padre è un controllo personalizzato che non implementa correttamente la tabulazione. Ad esempio, la proprietà MSAA State non viene mai impostata su STATE \_ SYSTEM \_ FOCUSABLE.
-   Un elemento che funge da contenitore per altri elementi è stato selezionato per la verifica, ma non supporta la navigazione tramite tastiera. Ad esempio, una barra degli strumenti e i relativi elementi figlio non sono accessibili usando il tasto TAB.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 