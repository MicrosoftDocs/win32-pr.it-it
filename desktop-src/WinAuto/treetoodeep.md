---
title: TreeTooDeep
description: TreeTooDeep
ms.assetid: 3FD4A1BE-4710-4A1F-9ED7-98D7FCBCD304
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201de20e9d1ccd34619cb711429d05fac15a507fc27a377211d5969a0a70b2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827586"
---
# <a name="treetoodeep"></a>TreeTooDeep

## <a name="text"></a>Testo

L'albero è {0} di livello più profondo.

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

La struttura ad albero degli elementi potrebbe essere troppo profonda.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento, perché l'attraversamento degli elementi potrebbe richiedere molto tempo e può sembrare ciclico.

## <a name="possible-causes"></a>Possibili cause

-   Più elementi o i relativi elementi padre sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà MsAA State non viene aggiornata correttamente.
-   L'interfaccia utente dell'applicazione è troppo complessa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Linee guida per l'interazione con l'esperienza utente - Tastiera](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 