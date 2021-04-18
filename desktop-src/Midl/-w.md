---
title: Opzione/W
description: L'opzione/W specifica il livello di avviso del compilatore MIDL. Il livello di avviso indica la gravità dell'avviso.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W switch MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299169"
---
# <a name="w-switch"></a>Opzione/W

L'opzione **/W** specifica il livello di avviso del compilatore MIDL. Il livello di avviso indica la gravità dell'avviso.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*level* 
</dt> <dd>

Specifica il livello di avviso, ovvero un numero intero compreso tra 0 e 4. Non è presente alcuno spazio tra l'opzione **/W** e la cifra che indica il valore a livello di avviso.

</dd> </dl>

## <a name="remarks"></a>Commenti

I livelli di avviso sono compresi tra 1 e 4 e il valore zero indica che non vengono visualizzate informazioni di avviso. L'avviso con la massima gravità è il livello 1. Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.



| Livello avvisi | Descrizione                                             | Esempio                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Nessun avviso.                                            |                                                                           |
| W1            | Avvisi gravi che possono causare errori dell'applicazione.      | Nessun handle di binding specificato, puntatori senza attributi, opzioni in conflitto. |
| W2            | Potrebbe causare problemi nell'ambiente operativo dell'utente. | La lunghezza dell'identificatore supera i 31 caratteri. Non è stato specificato alcun ARM di Unione predefinito.  |
| W3            | Riservato.                                               |                                                                           |
| W4            | Livello di avviso più basso.                                   | Costrutti non ANSI C.                                                    |



 

Gli avvisi sono diversi dagli errori. Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL. Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.

Il livello di avviso impostato dall'opzione **/W** può essere usato con l'opzione [**/WX**](-wx.md) per fare in modo che il compilatore MIDL interrompa l'elaborazione del file IDL.

Il comportamento dell'opzione **/W** è uguale a quello dell'opzione [**/warn**](-warn.md) .

## <a name="examples"></a>Esempio

**MIDL/W2 nomefile. idl**

**MIDL/W4 bar. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/warn**](-warn.md)
</dt> </dl>

 

 




