---
description: Esaminare l'elenco dei valori della modalità di conversione IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valori della modalità di conversione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406754"
---
# <a name="ime-conversion-mode-values"></a>Valori della modalità di conversione IME

Questi valori vengono usati con le [**funzioni ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| bit                      | Significato                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| CARATTERE \_ ALFANUMERICO IME CMODE \_ | Modalità di input alfanumerica. Si tratta dell'impostazione predefinita, definita come 0x0000.                          |
| IME \_ CMODE \_ CHARCODE     | Impostare su 1 se la modalità di input del codice carattere; 0 in caso di errore.                                          |
| IME \_ CMODE \_ EUDC         | Impostare su 1 se la modalità di conversione EUDC; 0 in caso di errore.                                               |
| IME \_ CMODE \_ FISSO        | **Windows Me/98, Windows 2000, Windows XP:** Impostare su 1 se la modalità di conversione fissa; 0 in caso di errore. |
| IME \_ CMODE \_ FULLSHAPE    | Impostare su 1 se la modalità forma completa; 0 se la modalità half shape.                                        |
| IME \_ CMODE \_ HANJACONVERT | Impostare su 1 se la modalità di conversione HANJA; 0 in caso di errore.                                                 |
| IME \_ CMODE \_ KATAKANA     | Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.                                            |
| IME \_ CMODE \_ NATIVO       | Impostare su 1 se la modalità NATIVA; 0 se la modalità ALPHANUMERIC.                                          |
| IME \_ CMODE \_ NOCONVERSION | Impostare su 1 per impedire l'elaborazione delle conversioni tramite IME. 0 in caso di errore.                           |
| IME \_ CMODE \_ ROMAN        | Impostare su 1 se la modalità di input ROMAN; 0 in caso di errore.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Impostare su 1 se la modalità Soft Keyboard; 0 in caso di errore.                                                 |
| SIMBOLO \_ CMODE IME \_       | Impostare su 1 se la modalità di conversione SYMBOL; 0 in caso di errore.                                             |



 

Tutti gli altri bit sono riservati.

 

 



