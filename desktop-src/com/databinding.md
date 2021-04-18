---
title: Data binding
description: Data binding
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300510"
---
# <a name="databinding"></a><span data-ttu-id="3541e-103">Data binding</span><span class="sxs-lookup"><span data-stu-id="3541e-103">Databinding</span></span>

<span data-ttu-id="3541e-104">È stato aggiunto un nuovo attributo DataBinding per consentire alle proprietà di distinguere tra le modifiche che comunicano solo quando lo stato attivo lascia il controllo o durante tutte le notifiche di modifica delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3541e-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="3541e-105">Il nuovo attributo, noto come ImmediateBind, consente ai controlli di distinguere due tipi diversi di proprietà associabili.</span><span class="sxs-lookup"><span data-stu-id="3541e-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="3541e-106">Un tipo di proprietà associabile deve inviare una notifica a ogni modifica apportata al database, ad esempio con un controllo casella di controllo in cui ogni modifica deve essere inviata al database sottostante anche se il controllo non ha perso lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3541e-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="3541e-107">Tuttavia, i controlli, ad esempio una casella di riepilogo, desiderano solo la modifica di una proprietà notificata al database quando il controllo perde lo stato attivo, poiché è possibile che l'utente abbia modificato la selezione evidenziata con i tasti di direzione prima di trovare l'impostazione desiderata, in modo che la notifica delle modifiche venga inviata al database ogni volta che l'utente preme il tasto di direzione.</span><span class="sxs-lookup"><span data-stu-id="3541e-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="3541e-108">La nuova proprietà bind immediata consente a singole proprietà associabili in un form di specificare questo comportamento, quando questo bit è impostato, tutte le modifiche verranno notificate.</span><span class="sxs-lookup"><span data-stu-id="3541e-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="3541e-109">Il nuovo bit ImmediateBind esegue il mapping ai nuovi \_ bit VARFLAG FIMMEDIATEBIND (0x80) e FUNCFLAG \_ FIMMEDIATEBIND (0x80) nelle enumerazioni VARFLAGS e FUNCFLAGS per l'interfaccia [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) che consente di controllare gli attributi delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3541e-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 