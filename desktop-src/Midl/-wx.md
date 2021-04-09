---
title: Opzione/WX
description: L'opzione/WX indica al compilatore MIDL di gestire tutti gli errori al livello di avviso specificato come errori.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX switch MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857502"
---
# <a name="wx-switch"></a>Opzione/WX

L'opzione **/WX** indica al compilatore MIDL di gestire tutti gli errori al livello di avviso specificato come errori.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Se si specifica l'opzione **/WX** e non si specifica l'opzione [**/W**](-w.md)*n* , tutti gli avvisi a livello predefinito, livello 1, vengono considerati errori.

L'opzione [**/W**](-w.md)*n* indica al compilatore di visualizzare tutti gli avvisi a livello *n* e **/WX** indirizza il compilatore alla gestione di tutti gli avvisi come errori. La combinazione di queste due opzioni indica al compilatore di gestire tutti gli avvisi a livello *n* come errori.

Gli errori sono diversi dagli avvisi. Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL. Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.

Avviso-livello zero (0) indica al compilatore MIDL di non visualizzare le informazioni di avviso. Quando le opzioni **/W0** e **/WX** vengono combinate, il compilatore MIDL disattiva tutte le informazioni sull'avviso. In questo caso, l'opzione **/WX** non ha alcun effetto.

## <a name="examples"></a>Esempio

**MIDL/WX nomefile. idl**

**MIDL/W3/WX nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




