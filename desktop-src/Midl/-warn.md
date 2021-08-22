---
title: Opzione /warn
description: L'opzione /warn specifica il livello di avviso del compilatore MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- Opzione /warn MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067457"
---
# <a name="warn-switch"></a>Opzione /warn

**L'opzione /warn** specifica il livello di avviso del compilatore MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*level* 
</dt> <dd>

Specifica il livello di avviso, un numero intero compreso tra 0 e 4. Non è presente alcuno spazio tra **l'opzione /warn** e la cifra che indica il valore a livello di avviso.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il livello di avviso indica la gravità dell'avviso. I livelli di avviso sono da 1 a 4, con un valore pari a zero che indica che non vengono visualizzate informazioni di avviso. L'avviso di gravità più alto è il livello 1. Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.



| Livello avvisi | Descrizione                                             | Esempio                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Nessun avviso.                                            |                                                                           |
| 1             | Avvisi gravi che possono causare errori dell'applicazione.      | Nessun handle di associazione specificato, puntatori senza attributi, opzioni in conflitto. |
| 2             | Può causare problemi nell'ambiente operativo dell'utente. | La lunghezza dell'identificatore supera i 31 caratteri. Nessun arm di unione predefinito specificato.  |
| 3             | Riservato.                                               |                                                                           |
| 4             | Livello minimo di avviso.                                   | Costrutti C non ANSI.                                                    |



 

Gli avvisi sono diversi dagli errori. Gli errori causano l'interruzione dell'elaborazione del file IDL da parte del compilatore MIDL. Gli avvisi causano la creazione di un messaggio informativo da parte del compilatore MIDL e la continuazione dell'elaborazione del file IDL.

Il livello di avviso impostato dall'opzione **/warn** può essere usato con l'opzione [**WX**](-wx.md) per causare l'interruzione dell'elaborazione del file IDL da parte del compilatore MIDL.

**L'opzione /warn** si comporta come l'opzione [**/W.**](-w.md)

## <a name="examples"></a>Esempio

**midl /warn2 filename.idl**

**midl /warn4 bar.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




