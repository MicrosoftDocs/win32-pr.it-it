---
description: Questi valori vengono utilizzati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valori della modalità frase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231741"
---
# <a name="ime-sentence-mode-values"></a>Valori della modalità frase IME

Questi valori vengono utilizzati con le funzioni [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| Costante                  | Definizione                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| \_SMODE IME \_ automatico     | L'IME esegue l'elaborazione della conversione in modalità automatica.               |
| \_SMODE IME \_ None          | Nessuna informazione per la frase.                                               |
| \_PHRASEPREDICT SMODE \_ IME | L'IME utilizza le informazioni sulla frase per stimare il carattere successivo.             |
| \_PLURALCLAUSE SMODE \_ IME  | L'IME utilizza le informazioni sulla clausola plurale per eseguire l'elaborazione della conversione. |
| \_SINGLECONVERT SMODE \_ IME | L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.        |
| \_conversazione SMODE \_ IME  | L'IME utilizza la modalità conversazione. Questa operazione è utile per le applicazioni di chat.      |



 

I bit da 16 a 31 sono riservati per l'uso di IME.

 

 



