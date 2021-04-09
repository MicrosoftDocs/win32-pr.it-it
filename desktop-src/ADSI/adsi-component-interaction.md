---
title: Interazione componente ADSI
description: Il componente Active Directory router popola una tabella del provider ADSI dai provider ADSI installati elencati nel registro di sistema quando riceve la prima richiesta dall'applicazione client.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730207"
---
# <a name="adsi-component-interaction"></a><span data-ttu-id="8d6b3-103">Interazione componente ADSI</span><span class="sxs-lookup"><span data-stu-id="8d6b3-103">ADSI Component Interaction</span></span>

<span data-ttu-id="8d6b3-104">Il componente Active Directory router popola una tabella del provider ADSI dai provider ADSI installati elencati nel registro di sistema quando riceve la prima richiesta dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="8d6b3-105">Per ulteriori informazioni sul Registro di sistema, vedere [installazione del componente provider di esempio](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="8d6b3-106">Le operazioni che effettuano una richiesta da una directory per un puntatore a un'interfaccia su un oggetto Active Directory passano attraverso una funzione (**GetObject** in Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C o C++) oppure un metodo di interfaccia ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="8d6b3-107">Nella figura seguente l'applicazione client ADSI passa una richiesta di associazione al componente del router ADSI (1).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="8d6b3-108">Il componente router identifica il ProgID per il provider dalla prima parte di ADsPath e utilizza [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per trovare il CLSID corrispondente nel registro di sistema (2) e carica il componente provider appropriato (3).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![interazioni dei componenti ADSI nel provider di esempio](images/dscspr.png)

<span data-ttu-id="8d6b3-110">Nella figura precedente il componente provider crea un oggetto Active Directory che rappresenta l'elemento directory denominata.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="8d6b3-111">Il componente del supporto ADSI esegue un **QueryInterface** sull'identificatore di interfaccia richiesto.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="8d6b3-112">Quando viene recuperato un puntatore a tale interfaccia (4), come con tutte le implementazioni client/server COM, viene quindi passato di nuovo al client (5) e da quel momento in poi l'applicazione client funziona direttamente con il componente provider (6).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 