---
title: Esecuzione di query sulle variabili di stato
description: L'interfaccia IUPnPService fornisce il metodo QueryStateVariable, che restituisce il valore di una variabile di stato specificata.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329591"
---
# <a name="querying-state-variables"></a><span data-ttu-id="3e783-103">Esecuzione di query sulle variabili di stato</span><span class="sxs-lookup"><span data-stu-id="3e783-103">Querying State Variables</span></span>

<span data-ttu-id="3e783-104">L'interfaccia [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fornisce il metodo [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , che restituisce il valore di una variabile di stato specificata.</span><span class="sxs-lookup"><span data-stu-id="3e783-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="3e783-105">Il forum di UPnP sconsiglia l'uso di [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="3e783-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="3e783-106">È stato suggerito ai writer di dispositivi di scrivere le azioni appropriate per fornire queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="3e783-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="3e783-107">I writer di dispositivi non sono obbligati a implementare **QueryStateVariable**.</span><span class="sxs-lookup"><span data-stu-id="3e783-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="3e783-108">Vedere la sezione [richiamo di azioni](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3e783-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




