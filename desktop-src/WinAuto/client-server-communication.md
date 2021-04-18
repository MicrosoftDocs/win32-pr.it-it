---
title: Comunicazione client/server
description: Il meccanismo WinEvents consente ai server di comunicare facilmente con i client di Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299337"
---
# <a name="clientserver-communication"></a><span data-ttu-id="f96cb-103">Comunicazione client/server</span><span class="sxs-lookup"><span data-stu-id="f96cb-103">Client/Server Communication</span></span>

<span data-ttu-id="f96cb-104">Il meccanismo [winEvents](winevents-overview.md) consente ai server di comunicare facilmente con i client di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="f96cb-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="f96cb-105">I client raccolgono spesso le informazioni rispondendo a WinEvents (ad esempio, seguendo lo stato attivo), ma sono gratuite per richiedere informazioni da un server in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="f96cb-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="f96cb-106">Per richiedere informazioni per un oggetto accessibile che genera un WinEvent, un client deve elaborare l'evento e stabilire una connessione con l'oggetto accessibile pertinente.</span><span class="sxs-lookup"><span data-stu-id="f96cb-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="f96cb-107">A tale scopo, il client esegue i sei passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f96cb-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="f96cb-108">Un server chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per generare una notifica WinEvent per ogni modifica apportata agli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f96cb-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="f96cb-109">Il codice di gestione di WinEvent in USER determina se le applicazioni client hanno registrato una [*funzione hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chiama la funzione di callback registrata.</span><span class="sxs-lookup"><span data-stu-id="f96cb-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="f96cb-110">Nella funzione di callback, il client richiede l'accesso all'oggetto che ha generato l'evento chiamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) o altre funzioni di recupero di oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="f96cb-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="f96cb-111">Per ulteriori informazioni, vedere [recupero di un oggetto IAccessible](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="f96cb-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="f96cb-112">Questa API Microsoft Active Accessibility invia all'applicazione server un messaggio [**WM \_ GetObject**](wm-getobject.md) per recuperare l'oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="f96cb-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="f96cb-113">In risposta a [**WM \_ GetObject**](wm-getobject.md), l'applicazione server restituisce zero o restituisce un valore che funge da riferimento unico all'oggetto che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="f96cb-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="f96cb-114">Se il server restituisce zero, Microsoft Active Accessibility crea un oggetto proxy e assegna al client l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f96cb-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="f96cb-115">In caso contrario, Microsoft Active Accessibility utilizza questo riferimento per recuperare l'indirizzo di un'interfaccia oggetto, ad esempio [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch**](idispatch-interface.md), e assegna tale indirizzo al client.</span><span class="sxs-lookup"><span data-stu-id="f96cb-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="f96cb-116">Una volta che il client dispone di un indirizzo di interfaccia, può chiamare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto accessibile per recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="f96cb-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f96cb-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f96cb-117">In this section</span></span>

-   [<span data-ttu-id="f96cb-118">WinEvents e Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="f96cb-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="f96cb-119">Funzionamento di WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="f96cb-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="f96cb-120">Recupero di un oggetto IAccessible</span><span class="sxs-lookup"><span data-stu-id="f96cb-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




