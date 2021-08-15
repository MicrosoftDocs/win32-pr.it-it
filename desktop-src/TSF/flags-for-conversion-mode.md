---
title: Flag per la modalità di conversione (Ctffunc.h)
description: I flag seguenti vengono usati come valore di GUID \_ COMPARTMENT \_ KEYBOARD \_ INPUTMODE \_ CONVERSION. È equivalente ai valori IME \_ CMODE per IMM32.
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
ms.openlocfilehash: 72c8c3a452e3115e66e4f0f6e75999cad9bce7e1eadf14b4cadd24fae640a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879217"
---
# <a name="flags-for-conversion-mode"></a>Flag per la modalità di conversione

I flag seguenti vengono usati come valore di [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ CONVERSION](predefined-compartments.md). È equivalente ai valori [IME \_ CMODE](../intl/ime-conversion-mode-values.md) per IMM32.



| Flag                             | valore  | Descrizione                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| VALORE \_ ALFANUMERICO TF CONVERSIONMODE \_ | 0x0000 | Impostare su 1 se è attiva la modalità ALFANUMERIC.                                  |
| TF \_ CONVERSIONMODE \_ NATIVE       | 0x0001 | Impostare su 1 se è attiva la modalità NATIVA. 0 se la modalità ALFANUMERIC.                |
| TF \_ CONVERSIONMODE \_ KATAKANA     | 0x0002 | Impostare su 1 se la modalità KATAKANA; 0 se è attiva la modalità HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Impostare su 1 se è attiva la modalità a forma intera. 0 se la modalità semi-forma.              |
| TF \_ CONVERSIONMODE \_ ROMAN        | 0x0010 | Impostare su 1 per impedire l'elaborazione delle conversioni tramite IME. 0 in caso no. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Impostare su 1 se la modalità di input del codice carattere; 0 in caso no.                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | Impostare su 1 se la modalità Soft Keyboard; 0 in caso di errore.                       |
| TF \_ CONVERSIONMODE \_ NOCONVERSION | 0x0100 | Impostare su 1 per impedire l'elaborazione delle conversioni tramite IME. 0 in caso no. |
| SIMBOLO \_ CONVERSIONMODE TF \_       | 0x0400 | Impostare su 1 se la modalità di conversione SYMBOL; 0 in caso no.                   |
| TF \_ CONVERSIONMODE \_ FIXED        | 0x0800 | Impostare su 1 se la modalità di conversione fissa è impostata su 1. 0 in caso di errore.                    |



 

I valori seguenti vengono usati come valore di [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ SENTENCE](predefined-compartments.md). È equivalente ai valori [IME \_ SMODE](../intl/ime-composition-string-values.md) per IMM32.



| Flag                            | valore  | Descrizione                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ NONE          | 0x0000 | Nessuna informazione per la frase.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | L'IME usa informazioni sulla clausola plurale per eseguire l'elaborazione della conversione. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.        |
| TF \_ SENTENCEMODE \_ AUTOMATIC     | 0x0004 | L'IME esegue l'elaborazione della conversione in modalità automatica.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | L'IME usa le informazioni sulle frasi per stimare il carattere successivo.             |
| CONVERSAZIONE TF \_ \_ SENTENCEMODE  | 0x0010 | L'IME usa la modalità conversazione. Ciò è utile per le applicazioni di chat.      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1.0 inWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Intestazione<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raggruppamenti predefiniti](predefined-compartments.md)
</dt> </dl>

 

