---
description: Questi valori vengono utilizzati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valori della modalità di conversione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129739"
---
# <a name="ime-conversion-mode-values"></a>Valori della modalità di conversione IME

Questi valori vengono utilizzati con le funzioni [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| bit                      | Significato                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| \_ \_ alfanumerico cmode IME | Modalità di input alfanumerico. Si tratta dell'impostazione predefinita, definita come 0x0000.                          |
| \_CHARCODE cmode \_ IME     | Impostare su 1 se la modalità di input del codice carattere; 0 in caso contrario.                                          |
| \_EUDC cmode \_ IME         | Impostare su 1 se la modalità di conversione EUDC; 0 in caso contrario.                                               |
| \_cmode IME \_ corretti        | **Windows Me/98, windows 2000, Windows XP:** Impostare su 1 se la modalità di conversione è fissa; 0 in caso contrario. |
| \_FULLSHAPE cmode \_ IME    | Impostare su 1 se la modalità di forma completa; 0 se la modalità a metà forma.                                        |
| \_HANJACONVERT cmode \_ IME | Impostare su 1 se la modalità di conversione HANJA; 0 in caso contrario.                                                 |
| \_katakana cmode \_ IME     | Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.                                            |
| IME \_ cmode \_ nativo       | Impostare su 1 se la modalità nativa; 0 se la modalità ALFANUMERICa.                                          |
| noconversione IME \_ cmode \_ | Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario.                           |
| IME \_ cmode \_ Roman        | Impostare su 1 se la modalità di input romana; 0 in caso contrario.                                                   |
| \_SOFTKBD cmode \_ IME      | Impostare su 1 se la modalità tastiera soft; 0 in caso contrario.                                                 |
| \_simbolo cmode \_ IME       | Impostare su 1 se la modalità di conversione del simbolo. 0 in caso contrario.                                             |



 

Tutti gli altri bit sono riservati.

 

 



