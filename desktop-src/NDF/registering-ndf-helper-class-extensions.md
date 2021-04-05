---
title: Registrazione delle estensioni di classe helper NDF
description: A ogni estensione della classe helper è associata una serie di chiavi del registro di sistema. Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714671"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="84dd9-104">Registrazione delle estensioni di classe helper NDF</span><span class="sxs-lookup"><span data-stu-id="84dd9-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="84dd9-105">A ogni estensione della classe helper è associata una serie di chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84dd9-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="84dd9-106">Alcune chiavi sono richieste da COM e alcune chiavi sono richieste da NDF.</span><span class="sxs-lookup"><span data-stu-id="84dd9-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="84dd9-107">Chiavi del registro di sistema COM</span><span class="sxs-lookup"><span data-stu-id="84dd9-107">COM Registry Keys</span></span>

<span data-ttu-id="84dd9-108">Le estensioni della classe helper devono essere implementate come server COM.</span><span class="sxs-lookup"><span data-stu-id="84dd9-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="84dd9-109">Per ogni estensione della classe helper è necessario completare la registrazione COM.</span><span class="sxs-lookup"><span data-stu-id="84dd9-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="84dd9-110">È necessario registrare il CLSID dell'oggetto, l'interfaccia [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) e l'interfaccia [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) .</span><span class="sxs-lookup"><span data-stu-id="84dd9-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="84dd9-111">La registrazione crea una serie di chiavi del registro di sistema correlate a COM per l'estensione della classe helper NDF.</span><span class="sxs-lookup"><span data-stu-id="84dd9-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="84dd9-112">Chiavi del registro di sistema NDF</span><span class="sxs-lookup"><span data-stu-id="84dd9-112">NDF Registry Keys</span></span>

<span data-ttu-id="84dd9-113">È necessario registrare le estensioni della classe helper prima di interagire con il Framework di diagnostica di rete e con altre classi helper correlate.</span><span class="sxs-lookup"><span data-stu-id="84dd9-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="84dd9-114">Questa operazione viene eseguita popolando il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84dd9-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="84dd9-115">Nella procedura seguente viene illustrato come aggiungere estensioni di classe helper al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84dd9-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="84dd9-116">Pubblicare i nomi delle classi helper implementate dalla DLL e le relative dipendenze creando una chiave per la DLL in</span><span class="sxs-lookup"><span data-stu-id="84dd9-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="84dd9-117">**HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class nome classe helper*</span><span class="sxs-lookup"><span data-stu-id="84dd9-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="84dd9-118">Sostituire *VendorName*, la *dll della classe helper* e il *nome della classe helper* con i valori definiti dall'utente, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="84dd9-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="84dd9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="84dd9-119">Value</span></span>               | <span data-ttu-id="84dd9-120">Type</span><span class="sxs-lookup"><span data-stu-id="84dd9-120">Type</span></span>    | <span data-ttu-id="84dd9-121">Significato</span><span class="sxs-lookup"><span data-stu-id="84dd9-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="84dd9-122">*NomeFornitore*</span><span class="sxs-lookup"><span data-stu-id="84dd9-122">*VendorName*</span></span>        | <span data-ttu-id="84dd9-123">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-123">REG\_SZ</span></span> | <span data-ttu-id="84dd9-124">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="84dd9-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="84dd9-125">*DLL della classe helper*</span><span class="sxs-lookup"><span data-stu-id="84dd9-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="84dd9-126">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-126">REG\_SZ</span></span> | <span data-ttu-id="84dd9-127">Nome della DLL senza estensione.</span><span class="sxs-lookup"><span data-stu-id="84dd9-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="84dd9-128">*Nome classe helper*</span><span class="sxs-lookup"><span data-stu-id="84dd9-128">*Helper Class Name*</span></span> | <span data-ttu-id="84dd9-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-129">REG\_SZ</span></span> | <span data-ttu-id="84dd9-130">Nome della classe helper da cui dipende la classe helper corrente.</span><span class="sxs-lookup"><span data-stu-id="84dd9-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="84dd9-131">In ogni chiave del *nome della classe helper* pubblicare le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="84dd9-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="84dd9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="84dd9-132">Value</span></span>         | <span data-ttu-id="84dd9-133">Type</span><span class="sxs-lookup"><span data-stu-id="84dd9-133">Type</span></span>       | <span data-ttu-id="84dd9-134">Significato</span><span class="sxs-lookup"><span data-stu-id="84dd9-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="84dd9-135">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="84dd9-135">**CLSID**</span></span>     | <span data-ttu-id="84dd9-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-136">REG\_SZ</span></span>    | <span data-ttu-id="84dd9-137">Stringa che contiene l'ID della classe COM della classe helper.</span><span class="sxs-lookup"><span data-stu-id="84dd9-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="84dd9-138">**Versione**</span><span class="sxs-lookup"><span data-stu-id="84dd9-138">**Version**</span></span>   | <span data-ttu-id="84dd9-139">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-139">REG\_SZ</span></span>    | <span data-ttu-id="84dd9-140">Stringa che contiene le versioni principale e secondaria della classe helper nel formato <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="84dd9-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="84dd9-141">**Pubblicato**</span><span class="sxs-lookup"><span data-stu-id="84dd9-141">**Published**</span></span> | <span data-ttu-id="84dd9-142">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="84dd9-142">REG\_DWORD</span></span> | <span data-ttu-id="84dd9-143">Il valore 1 indica che questa classe helper dovrebbe essere richiamata direttamente dal client di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="84dd9-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="84dd9-144">0 indica che può essere chiamato solo da un'altra classe helper.</span><span class="sxs-lookup"><span data-stu-id="84dd9-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="84dd9-145">**Parent**</span><span class="sxs-lookup"><span data-stu-id="84dd9-145">**Parent**</span></span>    | <span data-ttu-id="84dd9-146">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="84dd9-146">REG\_SZ</span></span>    | <span data-ttu-id="84dd9-147">Stringa che denomina la classe helper Microsoft estendibile che viene estesa.</span><span class="sxs-lookup"><span data-stu-id="84dd9-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="84dd9-148">Per ogni classe helper, pubblicare l'elenco degli attributi corrispondenti creando una chiave in</span><span class="sxs-lookup"><span data-stu-id="84dd9-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="84dd9-149">**HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class nome* \\ **MatchAttributes**</span><span class="sxs-lookup"><span data-stu-id="84dd9-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="84dd9-150">La chiave deve contenere uno o più valori (uno per ogni attributo) del tipo seguente.</span><span class="sxs-lookup"><span data-stu-id="84dd9-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="84dd9-151">Valore</span><span class="sxs-lookup"><span data-stu-id="84dd9-151">Value</span></span>             | <span data-ttu-id="84dd9-152">Type</span><span class="sxs-lookup"><span data-stu-id="84dd9-152">Type</span></span>                             | <span data-ttu-id="84dd9-153">Significato</span><span class="sxs-lookup"><span data-stu-id="84dd9-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="84dd9-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="84dd9-154">**AttributeName**</span></span> | <span data-ttu-id="84dd9-155">reg \_ SZ \| reg \_ DWORD \| reg \_ Binary</span><span class="sxs-lookup"><span data-stu-id="84dd9-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="84dd9-156">Valore che completa la coppia di nome e valore per un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="84dd9-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




