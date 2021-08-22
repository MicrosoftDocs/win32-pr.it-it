---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6bda8de3e07f0ac6be3aa3a2a7bd750508dead1f5c2662391a056b258b36d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644101"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Testo

La tabulazione in avanti e indietro non produce lo stesso elemento. Previsto {0} ma ricevuto {1}

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando si usa la navigazione da tastiera standard (TAB o MAIUSC+TAB), non è possibile ripetere il percorso di attraversamento attraverso l'albero degli elementi della destinazione di verifica se la direzione dell'attraversamento è inversa. Ad esempio, la tabulazione avanti (TAB) x volte dall'elemento A(0) all'elemento A(x) e quindi la tabulazione all'indietro (MAIUSC+TAB) x volte comporta la riconquista dello stato attivo dell'elemento A(0) tramite un set diverso di elementi intermedi.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione, perché l'attraversamento degli elementi appare irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

-   Più elementi o i relativi elementi padre sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà MSAA State non è impostata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 