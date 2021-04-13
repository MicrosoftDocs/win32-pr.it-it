---
title: Overload di IPropertyNotifySink
description: Overload di IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396646"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="d41f0-103">Overload di IPropertyNotifySink</span><span class="sxs-lookup"><span data-stu-id="d41f0-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="d41f0-104">Molti contenitori di controlli ActiveX implementano una finestra di esplorazione delle proprietà non modale.</span><span class="sxs-lookup"><span data-stu-id="d41f0-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="d41f0-105">Se le proprietà di un controllo vengono modificate tramite le pagine delle proprietà del controllo, le proprietà del controllo possono non essere sincronizzate con la visualizzazione del contenitore di tali proprietà (ovviamente, il controllo è sempre a destra).</span><span class="sxs-lookup"><span data-stu-id="d41f0-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="d41f0-106">Per assicurarsi che disponga sempre dei valori correnti per le proprietà di un controllo, un contenitore di controlli ActiveX può sovraccaricare l'interfaccia [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (Data Binding) e utilizzarla anche per ricevere una notifica della modifica di una proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="d41f0-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="d41f0-107">Questa tecnica è facoltativa e non è necessaria per i contenitori di controlli ActiveX o i controlli ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d41f0-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="d41f0-108">Si noti che un controllo deve usare [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) solo per data binding; è possibile utilizzare [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) per uno o entrambi gli scopi.</span><span class="sxs-lookup"><span data-stu-id="d41f0-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




