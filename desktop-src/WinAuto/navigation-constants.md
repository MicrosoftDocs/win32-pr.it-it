---
title: Costanti di navigazione (oleacc. h)
description: In questo argomento vengono descritti i valori costanti, definiti in oleacc. h, che indicano la direzione spaziale (su, giù, sinistra e destra) o logica (prima figlio, ultima, successiva e precedente) osservata quando i client utilizzano IAccessible accNavigate per spostarsi da un elemento dell'interfaccia utente all'altro nello stesso contenitore.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327476"
---
# <a name="navigation-constants"></a>Costanti di navigazione

In questo argomento vengono descritti i valori costanti, definiti in oleacc. h, che indicano la direzione *spaziale* (su, giù, sinistra e destra) o *logica* (prima figlio, ultima, successiva e precedente) osservata quando i client utilizzano [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per spostarsi da un elemento dell'interfaccia utente a un altro nello stesso contenitore. Per ulteriori informazioni, vedere [proprietà e metodi di navigazione degli oggetti](object-navigation-properties-and-methods.md).

Le costanti di navigazione di Microsoft Active Accessibility sono le seguenti:



| Costante                                                                                                                                                                  | Descrizione                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_**</dt> </dl>                   | Passare all'oggetto di pari livello posizionato sotto l'oggetto iniziale.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Passa al primo elemento figlio di questo oggetto. Quando si usa questo flag, il membro **LVAL** del parametro *VARSTART* deve essere CHILDID \_ self.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**\_LastChild NAVDIR**</dt> </dl>    | Passa all'ultimo elemento figlio di questo oggetto. Quando si usa questo flag, il membro **LVAL** del parametro *VARSTART* deve essere CHILDID \_ self.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR a \_ sinistra**</dt> </dl>                   | Passare all'oggetto di pari livello che si trova a sinistra dell'oggetto iniziale.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ successivo**</dt> </dl>                   | Passare al successivo oggetto logico; in genere, è un elemento di pari livello dell'oggetto iniziale.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ precedente**</dt> </dl>       | Passare all'oggetto logico precedente; in genere, è un elemento di pari livello dell'oggetto iniziale.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR a \_ destra**</dt> </dl>                | Passare all'oggetto di pari livello che si trova a destra dell'oggetto iniziale.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_**</dt> </dl>                         | Passare all'oggetto di pari livello posizionato sopra l'oggetto iniziale.<br/>                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



 

 





