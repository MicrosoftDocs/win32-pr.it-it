---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727519"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Testo

Questo elemento sembra essere a schede, ma non è nell'ordine di tabulazione.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Non è possibile accedere A un elemento attivabile mediante la navigazione da tastiera standard (TAB o MAIUSC + TAB). Ad esempio, l'elemento non è stato contrassegnato come tabulazione o è stato assegnato un indice di tabulazione. Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché:

-   L'elemento non è individuabile.
-   Se l'elemento è figlio di un controllo elenco personalizzato, i segnali che indicano l'elemento figlio possono essere spostati utilizzando la freccia o i tasti di pagina potrebbero essere mancanti.

## <a name="possible-causes"></a>Possibili cause

-   Il ruolo MSAA dell'elemento o del relativo elemento padre non è impostato correttamente. Se, ad esempio, tutti gli elementi dell'elenco in un controllo di visualizzazione elenco non vengono esposti tramite MSAA come oggetto \_ ListItem del sistema \_ del ruolo, la verifica non riesce perché le voci dell'elenco non sono accessibili tramite il tasto TAB.
-   L'elemento o il relativo padre è un controllo personalizzato che non implementa correttamente la tabulazione. Ad esempio, la proprietà dello stato MSAA non è mai impostata su stato di attivazione del sistema di stato \_ \_ .
-   Un elemento che funge da contenitore per altri elementi è stato selezionato per la verifica ma non supporta la navigazione da tastiera. Ad esempio, una barra degli strumenti e i relativi elementi figlio non sono accessibili utilizzando il tasto TAB.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 