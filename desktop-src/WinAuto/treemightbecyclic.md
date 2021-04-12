---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337670"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Testo

L'albero è a {0} livelli profondi. Questo potrebbe indicare che l'albero di accessibilità è ciclico e pertanto sembrerebbe essere infinito.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'albero degli elementi è ciclico e la profondità dell'albero può essere infinita.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché non esiste alcun limite evidente all'attraversamento degli elementi nell'applicazione di destinazione.

## <a name="possible-causes"></a>Possibili cause

Più elementi o i relativi padri sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà [stato](state-property.md) MSAA non viene aggiornata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Linee guida per l'interazione con l'esperienza utente Windows-tastiera](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 