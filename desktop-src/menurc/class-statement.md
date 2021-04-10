---
title: Istruzione CLASS
description: Definisce la classe della finestra di dialogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menu di istruzioni di classe e altre risorse
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963016"
---
# <a name="class-statement"></a>Istruzione CLASS

Definisce la classe della finestra di dialogo.

L'istruzione **Class** viene visualizzata nella sezione facoltativa prima del principale di un'istruzione della [**finestra di dialogo**](dialog-resource.md) . Se non viene specificata alcuna classe, viene usata la classe della finestra di dialogo standard.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*classe*
</dt> <dd>

Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo. Se la routine della finestra per la classe non elabora un messaggio inviato, deve chiamare la funzione [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) per garantire che tutti i messaggi vengano gestiti correttamente per la finestra di dialogo. Una classe privata può utilizzare **DefDlgProc** come routine della finestra predefinita. La classe deve essere registrata con il membro **cbWndExtra** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) impostata su **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'istruzione di **classe** deve essere utilizzata solo con casi particolari, perché esegue l'override della normale elaborazione di una finestra di dialogo. L'istruzione **Class** converte una finestra di dialogo in una finestra della classe specificata. a seconda della classe, questo può restituire risultati non desiderati. Non usare i nomi di classe di controllo ridefiniti con questa istruzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **Class** :

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DIALOGO**](dialog-resource.md)
</dt> </dl>

 

 