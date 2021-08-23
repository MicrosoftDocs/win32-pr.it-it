---
title: Istruzione CLASS
description: Definisce la classe della finestra di dialogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menu e altre risorse dell'istruzione CLASS
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a71485603944dc8b7eaf1a3a773051096776e6538aecdd8fb01396a3f0ea5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734658"
---
# <a name="class-statement"></a>Istruzione CLASS

Definisce la classe della finestra di dialogo.

**L'istruzione CLASS** viene visualizzata nella sezione facoltativa prima del [**main**](dialog-resource.md) di un'istruzione DIALOG. Se non viene specificata alcuna classe, viene usata la classe di finestra di dialogo standard.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Classe*
</dt> <dd>

Intero senza segno a 16 bit o stringa, racchiuso tra virgolette doppie ("), che identifica la classe della finestra di dialogo. Se la routine della finestra per la classe non elabora un messaggio inviato, deve chiamare la funzione [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) per assicurarsi che tutti i messaggi siano gestiti correttamente per la finestra di dialogo. Una classe privata può usare **DefDlgProc** come routine della finestra predefinita. La classe deve essere registrata con **il membro cbWndExtra** della [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) impostato su **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'istruzione CLASS** deve essere usata solo con casi speciali, perché esegue l'override della normale elaborazione di una finestra di dialogo. **L'istruzione CLASS** converte una finestra di dialogo in una finestra della classe specificata. a seconda della classe, ciò potrebbe dare risultati indesiderati. Non usare i nomi ridefiniti delle classi di controllo con questa istruzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso **dell'istruzione CLASS:**

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**Dialogo**](dialog-resource.md)
</dt> </dl>

 

 