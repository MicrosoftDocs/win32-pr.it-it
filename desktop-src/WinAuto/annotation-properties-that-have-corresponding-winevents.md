---
title: Proprietà di annotazione con WinEvents corrispondente
description: Prestare attenzione quando si esegue l'override delle proprietà che cambiano di frequente, in particolare quelle esaminate dai client come risultato di un WinEvent (ad esempio, stato, valore e, per alcuni controlli, le proprietà del nome).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399273"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Proprietà di annotazione con WinEvents corrispondente

Prestare attenzione quando si esegue l'override delle proprietà che cambiano di frequente, in particolare quelle esaminate dai client come risultato di un WinEvent (ad esempio, [**stato**](state-property.md), [**valore**](value-property.md)e, per alcuni controlli, le proprietà del [**nome**](name-property.md) ).

In molti casi, in particolare per i controlli USER e ComCtl, WinEvent segnala una modifica della proprietà prima che il proprietario del controllo riceva una notifica (in genere tramite [WM \_ Notify](../controls/wm-notify.md)). L'aggiornamento della proprietà tramite [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) nel \_ gestore di notifiche WM sarà troppo tardi; i client che utilizzano l'hook nel contesto avranno già eseguito l'accesso al valore precedente.

È possibile gestire questi tipi di proprietà usando oggetti server di callback (usando [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Tuttavia, il server non può usare alcuno stato aggiornato nel \_ gestore di notifiche WM perché tale gestore non sarà ancora stato chiamato. Ad esempio, anziché usare una variabile di valore corrente memorizzata nella cache che viene aggiornata nel gestore di notifiche WM e non è aggiornata \_ , l'oggetto di callback [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve inviare un messaggio direttamente al controllo per ottenere il valore effettivo corrente per generare la proprietà richiesta.

 

 