---
title: Associazione tardiva di ciò che accade dietro le quinte
description: In questo argomento viene descritto il funzionamento dell'associazione tardiva in ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, associazione tardiva, cosa accade dietro le quinte
- Binding AD, associazione tardiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474227"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="c3443-105">Associazione tardiva: cosa succede dietro le quinte?</span><span class="sxs-lookup"><span data-stu-id="c3443-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="c3443-106">Nell'elenco seguente viene descritto il processo generale per l'esecuzione di un'associazione tardiva:</span><span class="sxs-lookup"><span data-stu-id="c3443-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="c3443-107">Un elemento viene associato a un oggetto directory ADSI.</span><span class="sxs-lookup"><span data-stu-id="c3443-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="c3443-108">Ad esempio, "LDAP://CN = SergioMelchiori, OU = Sales, DC = Fabrikam, DC = COM" viene associato utilizzando l'associazione COM tardiva.</span><span class="sxs-lookup"><span data-stu-id="c3443-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="c3443-109">In questo modo ADSI chiama il metodo [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sull'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="c3443-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="c3443-110">ADSI trova un oggetto nella classe utente e crea un oggetto che supporta le interfacce appropriate, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="c3443-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="c3443-111">ADSI esegue una ricerca nel registro di sistema e trova i CLSID di estensione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c3443-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="c3443-112">Tenere presente che ADSI memorizza nella cache i dati.</span><span class="sxs-lookup"><span data-stu-id="c3443-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="c3443-113">Un elemento effettua una chiamata al metodo **MyNewMethod** .</span><span class="sxs-lookup"><span data-stu-id="c3443-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="c3443-114">ADSI cerca l'ID dispatch e gli ID dispatch per altre estensioni ADSI.</span><span class="sxs-lookup"><span data-stu-id="c3443-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="c3443-115">ADSI trova quindi l'estensione che serve questa chiamata e chiama l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.</span><span class="sxs-lookup"><span data-stu-id="c3443-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="c3443-116">L'estensione esegue la funzione.</span><span class="sxs-lookup"><span data-stu-id="c3443-116">The extension executes the function.</span></span>
-   <span data-ttu-id="c3443-117">A questo punto, il writer client richiama il metodo **YourNewMethod** usando l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per l'estensione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3443-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="c3443-118">L'implementazione **IDispatch** dell'estensione delega di nuovo **IDispatch** per ADSI.</span><span class="sxs-lookup"><span data-stu-id="c3443-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="c3443-119">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per ADSI cerca di nuovo l'estensione appropriata, o se stesso, chiama l'estensione appropriata usando l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per tale estensione.</span><span class="sxs-lookup"><span data-stu-id="c3443-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 