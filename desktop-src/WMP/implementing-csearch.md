---
title: Implementazione di CSearch
description: Implementazione di CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-in di Windows Media Player, classe CSearch
- plug-in, classe CSearch
- plug-in dell'interfaccia utente, classe CSearch
- Plug-in dell'interfaccia utente, classe CSearch
- Classe CSearch
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515613"
---
# <a name="implementing-csearch"></a><span data-ttu-id="069a1-109">Implementazione di CSearch</span><span class="sxs-lookup"><span data-stu-id="069a1-109">Implementing CSearch</span></span>

<span data-ttu-id="069a1-110">L'interfaccia **IWMPPluginUI** presenta diversi metodi che vengono chiamati da Windows Media Player in momenti diversi durante il ciclo di vita di un'istanza del plug-in.</span><span class="sxs-lookup"><span data-stu-id="069a1-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="069a1-111">La procedura guidata fornisce le implementazioni di base di questi metodi, nonché il costruttore e il distruttore della classe e altri metodi di classe.</span><span class="sxs-lookup"><span data-stu-id="069a1-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="069a1-112">Il file search. h deve essere modificato in modo che Windows Media Player possa comunicare con l'interfaccia utente, come descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="069a1-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="069a1-113">Affinché la classe CPluginWindow abbia accesso alla variabile membro privata m \_ spCore, è necessario eseguire una dichiarazione di classe Friend all'interno della definizione della classe CSearch, come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="069a1-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="069a1-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="069a1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="069a1-115">**Guida alla programmazione di plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="069a1-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




