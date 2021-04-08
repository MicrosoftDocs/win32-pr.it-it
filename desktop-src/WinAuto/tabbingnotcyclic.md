---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046967"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Testo

La tabulazione in questa applicazione non è ciclica. Il tabulazione in avanti o indietro {0} volte non torna allo stesso controllo.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando si usa la navigazione da tastiera standard (TAB o MAIUSC + TAB), non è possibile attraversare la struttura ad albero degli elementi della destinazione di verifica finché l'elemento iniziale diventa l'elemento finale (usando lo stesso numero di sequenze di tasti) invertendo la direzione di attraversamento. Ad esempio, la tabulazione in avanti (tabulazione) x volte dall'elemento A (0) all'elemento A (x) e la tabulazione indietro (MAIUSC + TAB) x volte non determinano il riattivazione dell'elemento A (0).

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché non esiste un modo prevedibile per tornare a un controllo dopo che è stato visitato.

## <a name="possible-causes"></a>Possibili cause

-   L'elemento o il relativo padre è un controllo personalizzato che non implementa correttamente la tabulazione. Ad esempio, la proprietà stato MSAA non è impostata correttamente.
-   Alcune applicazioni, ad esempio il blocco note, presentano questo comportamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 