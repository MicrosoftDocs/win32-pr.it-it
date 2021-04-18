---
title: Categorizzazione di proxy e Stub DCOM
description: Categorizzazione di proxy e Stub DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300540"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="fabf5-103">Categorizzazione di proxy e Stub DCOM</span><span class="sxs-lookup"><span data-stu-id="fabf5-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="fabf5-104">DCOM esegue il marshalling dei riferimenti agli oggetti costruendo OBJREF che contengono CLSID.</span><span class="sxs-lookup"><span data-stu-id="fabf5-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="fabf5-105">Questi CLSID sono vulnerabili agli attacchi di sicurezza perché le dll arbitrarie possono essere caricate durante il marshalling.</span><span class="sxs-lookup"><span data-stu-id="fabf5-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="fabf5-106">Tuttavia, \_ non \_ \_ è possibile specificare il flag di marshalling personalizzato EOAC quando si chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (vedere [**\_ \_ funzionalità di autenticazione Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="fabf5-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="fabf5-107">L'impostazione di questo flag consente di proteggere la sicurezza del server quando si utilizza DCOM perché riduce le probabilità di esecuzione di dll arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="fabf5-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="fabf5-108">Quando questo flag è impostato, il server consente il marshalling solo dei CLSID implementati in ole32.dll, comadmin.dll, comsvcs.dll o es.dll o che implementano l' \_ ID di categoria del gestore di marshalling CATID.</span><span class="sxs-lookup"><span data-stu-id="fabf5-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="fabf5-109">\_Il gestore di marshalling CATID è un GUID della categoria di componenti che può essere associato a un CLSID sottoposto a marshalling personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fabf5-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="fabf5-110">Le interfacce sottoposte a marshalling personalizzato con questo CLSID sono consentite quando EOAC \_ non \_ \_ è impostato alcun marshalling personalizzato tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="fabf5-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fabf5-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fabf5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fabf5-112">Categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="fabf5-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 