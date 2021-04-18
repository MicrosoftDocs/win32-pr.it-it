---
description: Un IME implementa una funzionalità denominata &\# 0034; riconversione&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Utilizzo della riconversione con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305632"
---
# <a name="using-reconversion-with-an-ime"></a>Utilizzo della riconversione con un IME

Un IME implementa una funzionalità denominata "riconversione". In genere l'IMM determina gli elenchi di candidati solo in base alle voci digitate dall'utente. La riconversione consente a IMM di determinare uno o più candidati in base alla frase che lo contiene (contesto). I tipi di riconversione definiti sono semplici, normali e avanzati.

La riconversione è utile quando un utente nota un errore di composizione in un documento. L'utente può selezionare l'errore e scegliere riconversione da un menu. L'IME usa il contesto per determinare la sostituzione migliore. L'applicazione può usare [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) per supportare la riconversione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di gestione metodi di input](using-input-method-manager.md)
</dt> </dl>

 

 



