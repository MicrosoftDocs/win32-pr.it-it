---
title: Opzione /W
description: L'opzione /W specifica il livello di avviso del compilatore MIDL. Il livello di avviso indica la gravità dell'avviso.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- Opzione /W MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b2d4a762a7fbb1bba00f8804e8e43a77ad8183a744add63fcf0d37c86d54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913671"
---
# <a name="w-switch"></a>Opzione /W

**L'opzione /W** specifica il livello di avviso del compilatore MIDL. Il livello di avviso indica la gravità dell'avviso.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*level* 
</dt> <dd>

Specifica il livello di avviso, un numero intero compreso tra 0 e 4. Non è disponibile spazio tra **l'opzione /W** e la cifra che indica il valore a livello di avviso.

</dd> </dl>

## <a name="remarks"></a>Commenti

I livelli di avviso sono da 1 a 4, con un valore pari a zero che indica che non vengono visualizzate informazioni di avviso. L'avviso con la gravità più alta è il livello 1. Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.



| Livello avvisi | Descrizione                                             | Esempio                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Nessun avviso.                                            |                                                                           |
| W1            | Avvisi gravi che possono causare errori dell'applicazione.      | Nessun handle di associazione specificato, puntatori senza attributi, opzioni in conflitto. |
| W2            | Può causare problemi nell'ambiente operativo dell'utente. | La lunghezza dell'identificatore supera i 31 caratteri. Nessun arm di unione predefinito specificato.  |
| W3            | Riservato.                                               |                                                                           |
| W4            | Livello di avviso più basso.                                   | Costrutti C non ANSI.                                                    |



 

Gli avvisi sono diversi dagli errori. Gli errori causano l'arresto dell'elaborazione del file IDL da parte del compilatore MIDL. Gli avvisi causano la creazione di un messaggio informativo da parte del compilatore MIDL e la continuazione dell'elaborazione del file IDL.

Il livello di avviso impostato dall'opzione **/W** può essere usato con l'opzione [**/WX**](-wx.md) per arrestare l'elaborazione del file IDL da parte del compilatore MIDL.

**L'opzione /W** si comporta come l'opzione [**/warn.**](-warn.md)

## <a name="examples"></a>Esempio

**midl /W2 filename.idl**

**midl /W4 bar.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/warn**](-warn.md)
</dt> </dl>

 

 




