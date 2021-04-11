---
title: Come ADSI integra le estensioni
description: Linee guida che descrivono il modo in cui ADSI interagisce con le estensioni.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- estensioni ADSI
- ADSI ed estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047357"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="e9fa8-105">Come ADSI integra le estensioni</span><span class="sxs-lookup"><span data-stu-id="e9fa8-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="e9fa8-106">Le linee guida seguenti descrivono il modo in cui ADSI interagisce con le estensioni:</span><span class="sxs-lookup"><span data-stu-id="e9fa8-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="e9fa8-107">Un elemento viene associato a un oggetto directory ADSI.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="e9fa8-108">Ad esempio, "LDAP://CN = SergioMelchiori, OU = Sales, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="e9fa8-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="e9fa8-109">ADSI indica che l'oggetto si trova nella classe **User** .</span><span class="sxs-lookup"><span data-stu-id="e9fa8-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="e9fa8-110">ADSI esegue una ricerca nel registro di sistema e identifica i CLSID di estensione per l' **utente**.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="e9fa8-111">Tenere presente che ADSI memorizza nella cache i dati.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="e9fa8-112">Un elemento chiama il metodo **QueryInterface** per IID \_ IMyExtension.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="e9fa8-113">ADSI Cerca le interfacce associate all'oggetto **utente** , iniziando con le proprie interfacce, quindi esaminando le interfacce di estensione.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="e9fa8-114">Se viene trovata una corrispondenza, ADSI crea un'istanza del componente che supporta IID \_ IMyExtension e chiama **QueryInterface** per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="e9fa8-115">Viene restituita l'interfaccia risultante.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="e9fa8-116">L'utente usa questa interfaccia per chiamare i metodi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="e9fa8-117">Il client chiama quindi **QueryInterface** per IID \_ IYourExtension, che si trova in un componente diverso.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="e9fa8-118">Questo componente delega la chiamata **QueryInterface** all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator, che si verifica come ADSI.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="e9fa8-119">Anche in questo caso, ADSI Cerca le interfacce e crea l'istanza del componente.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 