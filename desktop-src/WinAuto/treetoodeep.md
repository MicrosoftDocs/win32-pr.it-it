---
title: TreeTooDeep
description: TreeTooDeep
ms.assetid: 3FD4A1BE-4710-4A1F-9ED7-98D7FCBCD304
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681a929eca288584e9bd9ccd7b32920b10a72131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728530"
---
# <a name="treetoodeep"></a>TreeTooDeep

## <a name="text"></a>Testo

L'albero è a {0} livelli profondi.

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

La struttura ad albero degli elementi potrebbe essere troppo profonda.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché l'attraversamento degli elementi sembra richiedere molto tempo e può sembrare ciclico.

## <a name="possible-causes"></a>Possibili cause

-   Più elementi o i relativi padri sono controlli personalizzati che non implementano correttamente la tabulazione. Ad esempio, la proprietà stato MSAA non viene aggiornata correttamente.
-   L'interfaccia utente dell'applicazione è eccessivamente complessa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per la progettazione dell'interfaccia utente della tastiera](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Linee guida per l'interazione con l'esperienza utente Windows-tastiera](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 