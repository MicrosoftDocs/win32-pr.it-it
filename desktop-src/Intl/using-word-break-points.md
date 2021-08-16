---
description: Quando l'applicazione ha a che fare con parole intere, le posizioni valide per il cursore sono contrassegnate dal valore del membro fWordStop della struttura SCRIPT \_ LOGATTR. Questo valore viene recuperato effettuando una chiamata a ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Uso dei punti di interruzione di parola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733d761d15299e02fbfb84d541a7ceba5d4d77a9b57e0280bfeedee24532d8cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146864"
---
# <a name="using-word-break-points"></a>Uso dei punti di interruzione di parola

Quando l'applicazione ha a che fare con parole intere, le posizioni valide per il cursore sono contrassegnate dal valore del membro **fWordStop** della [**struttura SCRIPT \_ LOGATTR.**](/windows/win32/api/usp10/ns-usp10-script_logattr) Questo valore viene recuperato effettuando una chiamata a [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Le posizioni valide per le righe di interruzione tra le parole sono contrassegnate dal **valore fSoftBreak** recuperato da [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



