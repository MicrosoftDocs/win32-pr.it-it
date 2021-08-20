---
description: Esaminare l'elenco dei valori della modalità di conversione IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valori della modalità di conversione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aa2f400dbf75346b537df2a0c724ea0a241a6c3b32ef23b2f27a2ce5d075e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810381"
---
# <a name="ime-conversion-mode-values"></a>Valori della modalità di conversione IME

Questi valori vengono usati con le [**funzioni ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)



| bit                      | Significato                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE \_ ALFANUMERICO | Modalità di input alfanumerico. Si tratta dell'impostazione predefinita, definita come 0x0000.                          |
| IME \_ CMODE \_ CHARCODE     | Impostare su 1 se la modalità di input del codice carattere; 0 in caso no.                                          |
| IME \_ CMODE \_ EUDC         | Impostare su 1 se la modalità di conversione EUDC; 0 in caso no.                                               |
| IME \_ CMODE \_ FIXED        | **Windows Me/98, Windows 2000, Windows XP:** Impostare su 1 se la modalità di conversione fissa è impostata su 1. 0 in caso no. |
| IME \_ CMODE \_ FULLSHAPE    | Impostare su 1 se è attiva la modalità a forma intera. 0 se la modalità semi-forma.                                        |
| IME \_ CMODE \_ HANJACONVERT | Impostare su 1 se la modalità di conversione HANJA; 0 in caso no.                                                 |
| IME \_ CMODE \_ KATAKANA     | Impostare su 1 se la modalità KATAKANA; 0 se è attiva la modalità HIRAGANA.                                            |
| IME \_ CMODE \_ NATIVO       | Impostare su 1 se è attiva la modalità NATIVA. 0 se la modalità ALPHANUMERIC.                                          |
| IME \_ CMODE \_ NOCONVERSION | Impostare su 1 per impedire l'elaborazione delle conversioni tramite IME. 0 in caso no.                           |
| IME \_ CMODE \_ ROMAN        | Impostare su 1 se la modalità di input ROMAN; 0 in caso no.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Impostare su 1 se la modalità Soft Keyboard; 0 in caso no.                                                 |
| SIMBOLO \_ \_ CMODE IME       | Impostare su 1 se la modalità di conversione SYMBOL; 0 in caso no.                                             |



 

Tutti gli altri bit sono riservati.

 

 



