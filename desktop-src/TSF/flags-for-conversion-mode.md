---
title: Flag per la modalità di conversione (Ctffunc. h)
description: I flag seguenti vengono usati come valore della \_ conversione INPUTMODE della tastiera del raggruppamento GUID \_ \_ \_ . Equivale ai \_ valori cmode IME per imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Flag per la modalità di conversione Framework servizi di testo
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120066"
---
# <a name="flags-for-conversion-mode"></a>Flag per la modalità di conversione

I flag seguenti vengono usati come valore della [ \_ \_ \_ \_ conversione INPUTMODE della tastiera del raggruppamento GUID](predefined-compartments.md). Equivale ai valori [ \_ cmode IME](../intl/ime-conversion-mode-values.md) per imm32.



| Flag                             | valore  | Descrizione                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| \_CONVERSIONMODE \_ ALFANUMERICo TF | 0x0000 | Impostare su 1 se la modalità ALFANUMERICa.                                  |
| TF \_ CONVERSIONMODE \_ nativo       | 0x0001 | Impostare su 1 se la modalità nativa; 0 se la modalità ALFANUMERICa.                |
| \_CONVERSIONMODE \_ katakana     | 0x0002 | Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Impostare su 1 se la modalità di forma completa; 0 se la modalità a metà forma.              |
| TF \_ CONVERSIONMODE \_ Roman        | 0x0010 | Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Impostare su 1 se la modalità di input del codice carattere; 0 in caso contrario.                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | Impostare su 1 se la modalità tastiera soft; 0 in caso contrario.                       |
| TF \_ CONVERSIONMODE \_ noconversione | 0x0100 | Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario. |
| \_simbolo TF CONVERSIONMODE \_       | 0x0400 | Impostare su 1 se la modalità di conversione del simbolo. 0 in caso contrario.                   |
| \_CONVERSIONMODE TF \_ fisso        | 0x0800 | Impostare su 1 se la modalità di conversione è fissa; 0 in caso contrario.                    |



 

I valori seguenti vengono usati come valore della [ \_ \_ \_ \_ frase INPUTMODE della tastiera del raggruppamento GUID](predefined-compartments.md). Equivale ai valori [ \_ SMODE IME](../intl/ime-composition-string-values.md) per imm32.



| Flag                            | valore  | Descrizione                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ None          | 0x0000 | Nessuna informazione per la frase.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | L'IME utilizza le informazioni sulla clausola plurale per eseguire l'elaborazione della conversione. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.        |
| TF \_ SENTENCEMODE \_ automatico     | 0x0004 | L'IME esegue l'elaborazione della conversione in modalità automatica.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | L'IME utilizza le informazioni sulla frase per stimare il carattere successivo.             |
| \_conversazione TF SENTENCEMODE \_  | 0x0010 | L'IME utilizza la modalità conversazione. Questa operazione è utile per le applicazioni di chat.      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 onWindows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Intestazione<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raggruppamenti predefiniti](predefined-compartments.md)
</dt> </dl>

 

