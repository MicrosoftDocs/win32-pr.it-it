---
description: Esaminare l'elenco dei valori della modalità frase IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valori della modalità frase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406764"
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

 

 



