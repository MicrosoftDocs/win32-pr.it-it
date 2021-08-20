---
description: Esaminare l'elenco dei valori della modalità frase IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valori della modalità frase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146130"
---
# <a name="ime-sentence-mode-values"></a>Valori della modalità frase IME

Questi valori vengono usati con le [**funzioni ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| Costante                  | Definizione                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | L'IME esegue l'elaborazione della conversione in modalità automatica.               |
| IME \_ SMODE \_ NONE          | Nessuna informazione per la frase.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | L'IME usa le informazioni sulle frasi per stimare il carattere successivo.             |
| IME \_ SMODE \_ PLURALCLAUSE  | L'IME usa informazioni sulla clausola plurale per eseguire l'elaborazione della conversione. |
| IME \_ SMODE \_ SINGLECONVERT | L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.        |
| CONVERSAZIONE \_ SMODE IME \_  | L'IME usa la modalità conversazione. Ciò è utile per le applicazioni di chat.      |



 

I bit da 16 a 31 sono riservati per l'uso IME.

 

 



