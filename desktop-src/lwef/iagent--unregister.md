---
title: Annullare la registrazione di IAgent
description: Annullare la registrazione di IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872509"
---
# <a name="iagentunregister"></a><span data-ttu-id="01d39-103">IAgent:: Annulla registrazione</span><span class="sxs-lookup"><span data-stu-id="01d39-103">IAgent::Unregister</span></span>

<span data-ttu-id="01d39-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01d39-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="01d39-105">Scarica i dati di tipo carattere per il carattere specificato dalla raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="01d39-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="01d39-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="01d39-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="01d39-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span><span class="sxs-lookup"><span data-stu-id="01d39-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="01d39-108">ID sink di notifica.</span><span class="sxs-lookup"><span data-stu-id="01d39-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="01d39-109">Utilizzare questo metodo quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="01d39-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="01d39-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="01d39-110">See Also</span></span>

[<span data-ttu-id="01d39-111">**IAgent:: Register**</span><span class="sxs-lookup"><span data-stu-id="01d39-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 