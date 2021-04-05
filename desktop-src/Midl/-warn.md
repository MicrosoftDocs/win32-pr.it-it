---
title: opzione/warn
description: L'opzione/warn specifica il livello di avviso del compilatore MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn switch MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718199"
---
# <a name="warn-switch"></a>opzione/warn

L'opzione **/warn** specifica il livello di avviso del compilatore MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*level* 
</dt> <dd>

Specifica il livello di avviso, ovvero un numero intero compreso tra 0 e 4. Non è presente alcuno spazio tra l'opzione **/warn** e la cifra che indica il valore a livello di avviso.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il livello di avviso indica la gravità dell'avviso. I livelli di avviso sono compresi tra 1 e 4 e il valore zero indica che non vengono visualizzate informazioni di avviso. L'avviso con la massima gravità è il livello 1. Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.



| Livello avvisi | Descrizione                                             | Esempio                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Nessun avviso.                                            |                                                                           |
| 1             | Avvisi gravi che possono causare errori dell'applicazione.      | Nessun handle di binding specificato, puntatori senza attributi, opzioni in conflitto. |
| 2             | Potrebbe causare problemi nell'ambiente operativo dell'utente. | La lunghezza dell'identificatore supera i 31 caratteri. Non è stato specificato alcun ARM di Unione predefinito.  |
| 3             | Riservato.                                               |                                                                           |
| 4             | Livello di avviso più basso.                                   | Costrutti non ANSI C.                                                    |



 

Gli avvisi sono diversi dagli errori. Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL. Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.

Il livello di avviso impostato dall'opzione **/warn** può essere usato con l'opzione [**WX**](-wx.md) per fare in modo che il compilatore MIDL interrompa l'elaborazione del file IDL.

Il comportamento dell'opzione **/warn** è uguale a quello dell'opzione [**/W**](-w.md) .

## <a name="examples"></a>Esempio

**MIDL/warn2 nomefile. idl**

**MIDL/warn4 bar. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




