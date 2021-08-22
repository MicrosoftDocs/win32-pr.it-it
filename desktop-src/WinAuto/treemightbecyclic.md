---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614437"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Testo

L'albero è {0} a livello di livello. Ciò potrebbe indicare che l'albero di accessibilità è ciclico e quindi sembra infinito.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'albero degli elementi è ciclico e la profondità dell'albero potrebbe essere infinita.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione, perché non vi sarà alcun limite apparente all'attraversamento degli elementi nell'applicazione di destinazione.

## <a name="possible-causes"></a>Possibili cause

Più elementi o i relativi elementi padre sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà MSAA [State](state-property.md) non viene aggiornata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Linee guida per l'interazione con l'esperienza utente - Tastiera](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 