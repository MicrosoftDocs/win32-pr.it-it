---
title: Costanti di navigazione (Oleacc.h)
description: Questo argomento descrive i valori costanti, definiti in oleacc.h, che indicano la direzione spaziale (su, giù, sinistra e destra) o logica (primo figlio, ultimo, successivo e precedente) osservata quando i client usano IAccessible accNavigate per spostarsi da un elemento dell'interfaccia utente a un altro all'interno dello stesso contenitore.
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
ms.openlocfilehash: b3e5c3a39c1b628ea03d1e036265ba7787e15bb70ce550e06b43b8efcd02c14a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998171"
---
# <a name="navigation-constants"></a>Costanti di navigazione

Questo argomento descrive i valori costanti, definiti in oleacc.h, che indicano la direzione spaziale *(su,* giù, sinistra e destra) o logica *(primo* figlio, ultimo, successivo e precedente) osservata quando i client usano [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per spostarsi da un elemento dell'interfaccia utente a un altro all'interno dello stesso contenitore. Per altre informazioni, vedere [Proprietà e metodi di navigazione degli oggetti.](object-navigation-properties-and-methods.md)

Le Microsoft Active Accessibility di navigazione sono le seguenti:



| Costante                                                                                                                                                                  | Descrizione                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_ DOWN**</dt> </dl>                   | Passare all'oggetto di pari livello che si trova sotto l'oggetto iniziale.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Passare al primo elemento figlio di questo oggetto. Quando si usa questo flag, il membro **lVal** del *parametro varStart* deve essere CHILDID \_ SELF.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | Passare all'ultimo elemento figlio di questo oggetto. Quando si usa questo flag, il membro **lVal** del *parametro varStart* deve essere CHILDID \_ SELF.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR \_ A SINISTRA**</dt> </dl>                   | Passare all'oggetto di pari livello a sinistra dell'oggetto iniziale.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ NEXT**</dt> </dl>                   | Passare all'oggetto logico successivo. in genere è un elemento di pari livello dell'oggetto iniziale.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ PRECEDENTE**</dt> </dl>       | Passare all'oggetto logico precedente. in genere è un elemento di pari livello dell'oggetto iniziale.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ A DESTRA**</dt> </dl>                | Passare all'oggetto di pari livello che si trova a destra dell'oggetto iniziale.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_ UP**</dt> </dl>                         | Passare all'oggetto di pari livello che si trova sopra l'oggetto iniziale.<br/>                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



 

 





