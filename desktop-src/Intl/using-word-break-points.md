---
description: Quando l'applicazione sta gestendo parole intere, le posizioni valide per il punto di inserimento sono contrassegnate dal valore del membro fWordStop della \_ struttura LOGATTR dello script. Questo valore viene recuperato effettuando una chiamata a ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Uso di punti di interruzioni di Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234188"
---
# <a name="using-word-break-points"></a>Uso di punti di interruzioni di Word

Quando l'applicazione sta gestendo parole intere, le posizioni valide per il punto di inserimento sono contrassegnate dal valore del membro **fWordStop** della [**struttura \_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Questo valore viene recuperato effettuando una chiamata a [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Le posizioni valide per suddividere le righe tra le parole sono contrassegnate dal valore **fSoftBreak** recuperato da [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



