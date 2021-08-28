---
title: Proprietà di annotazione con WinEvent corrispondenti
description: Prestare attenzione quando si esegue l'override di proprietà che cambiano di frequente, in particolare quelle esaminate dai client come risultato di un WinEvent (ad esempio State, Value e, per alcuni controlli, le proprietà Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753a17498daf9966ed1c3dfa98dc64fbdb2290011842c4fe9c194f50bf408ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098511"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Proprietà di annotazione con WinEvent corrispondenti

Prestare attenzione quando si esegue l'override di proprietà che cambiano di frequente, in particolare quelle esaminate dai client come risultato di un WinEvent (ad esempio [**State,**](state-property.md) [**Value**](value-property.md)e, per alcuni controlli, le proprietà [**Name).**](name-property.md)

In molti casi, in particolare per i controlli USER e ComCtl, il WinEvent che segnala una modifica della proprietà viene inviato prima che il proprietario del controllo venga notificato (in genere tramite [WM \_ NOTIFY).](../controls/wm-notify.md) L'aggiornamento della proprietà [**tramite SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) nel gestore WM NOTIFY sarà troppo tardi. I client che usano l'hook nel contesto avranno già \_ eseguito l'accesso al valore precedente.

È possibile gestire questi tipi di proprietà usando oggetti server di callback [**(tramite SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Tuttavia, il server non può usare alcuno stato aggiornato nel gestore WM NOTIFY perché tale \_ gestore non sarà ancora stato chiamato. Ad esempio, invece di usare una variabile di valore corrente memorizzata nella cache aggiornata nel gestore WM NOTIFY e non aggiornata, l'oggetto \_ callback [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve inviare un messaggio direttamente al controllo per ottenere il valore corrente reale per generare la proprietà richiesta.

 

 