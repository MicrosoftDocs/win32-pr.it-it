---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117986"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Testo

La tabulazione all'indietro e in avanti non produce lo stesso elemento. Prevista {0} ma ricevuta {1}

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando si usa la navigazione da tastiera standard (TAB o MAIUSC + TAB), non è possibile ripetere il percorso di attraversamento attraverso l'albero degli elementi della destinazione di verifica se la direzione di attraversamento è invertita. Ad esempio, la tabulazione in avanti (tabulazione) x volte dall'elemento A (0) all'elemento A (x) e quindi alla tabulazione indietro (MAIUSC + TAB) x volte genera l'elemento A (0) riottenendo lo stato attivo tramite un set di elementi intermedi diverso.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché gli elementi attraversati sembrano imprevedibili e imprevedibili.

## <a name="possible-causes"></a>Possibili cause

-   Più elementi o i relativi padri sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà stato MSAA non è impostata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 