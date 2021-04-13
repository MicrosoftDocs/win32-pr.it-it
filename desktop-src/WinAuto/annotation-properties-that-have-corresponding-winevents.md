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
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="23494-103">Proprietà di annotazione con WinEvents corrispondente</span><span class="sxs-lookup"><span data-stu-id="23494-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="23494-104">Prestare attenzione quando si esegue l'override delle proprietà che cambiano di frequente, in particolare quelle esaminate dai client come risultato di un WinEvent (ad esempio, [**stato**](state-property.md), [**valore**](value-property.md)e, per alcuni controlli, le proprietà del [**nome**](name-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="23494-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="23494-105">In molti casi, in particolare per i controlli USER e ComCtl, WinEvent segnala una modifica della proprietà prima che il proprietario del controllo riceva una notifica (in genere tramite [WM \_ Notify](../controls/wm-notify.md)).</span><span class="sxs-lookup"><span data-stu-id="23494-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="23494-106">L'aggiornamento della proprietà tramite [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) nel \_ gestore di notifiche WM sarà troppo tardi; i client che utilizzano l'hook nel contesto avranno già eseguito l'accesso al valore precedente.</span><span class="sxs-lookup"><span data-stu-id="23494-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="23494-107">È possibile gestire questi tipi di proprietà usando oggetti server di callback (usando [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Tuttavia, il server non può usare alcuno stato aggiornato nel \_ gestore di notifiche WM perché tale gestore non sarà ancora stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="23494-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="23494-108">Ad esempio, anziché usare una variabile di valore corrente memorizzata nella cache che viene aggiornata nel gestore di notifiche WM e non è aggiornata \_ , l'oggetto di callback [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve inviare un messaggio direttamente al controllo per ottenere il valore effettivo corrente per generare la proprietà richiesta.</span><span class="sxs-lookup"><span data-stu-id="23494-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 