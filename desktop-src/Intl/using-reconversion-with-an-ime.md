---
description: Un IME implementa una funzionalità denominata &\# 0034;riconversione&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Uso della riconversione con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146844"
---
# <a name="using-reconversion-with-an-ime"></a>Uso della riconversione con un IME

Un IME implementa una funzionalità denominata "riconversione". In genere l'IMM determina gli elenchi di candidati in base solo alle voci digitate dall'utente. La riconversione consente a IMM di determinare uno o più candidati in base alla frase contenitore (contesto). I tipi di riconversione definiti sono semplici, normali e migliorati.

La riconversione è utile quando un utente nota un errore di composizione in un documento. L'utente può selezionare l'errore e scegliere riconversione da un menu. L'IME usa il contesto per determinare la sostituzione migliore. L'applicazione può usare [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) per supportare la riconversione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Gestione metodi di input](using-input-method-manager.md)
</dt> </dl>

 

 



