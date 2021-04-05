---
title: Accesso alla cache delle proprietà con le interfacce IADsProperty
description: Le interfacce IADsProperty sono costituite da IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Accesso alla cache delle proprietà direttamente con le interfacce IADsProperty ADSI
- ADSI cache proprietà
- ADSI cache proprietà, uso delle interfacce IADsProperty per accedere alla cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2019
ms.locfileid: "103956099"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a><span data-ttu-id="35b94-106">Accesso alla cache delle proprietà con le interfacce IADsProperty</span><span class="sxs-lookup"><span data-stu-id="35b94-106">Accessing Property Cache with IADsProperty Interfaces</span></span>

<span data-ttu-id="35b94-107">Le interfacce [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) sono costituite da [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span><span class="sxs-lookup"><span data-stu-id="35b94-107">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interfaces consist of [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span></span> <span data-ttu-id="35b94-108">Queste interfacce forniscono metodi per accedere direttamente e modificare le proprietà di una cache di oggetti.</span><span class="sxs-lookup"><span data-stu-id="35b94-108">These interfaces provide methods to directly access and manipulate the properties of an object cache.</span></span> <span data-ttu-id="35b94-109">Una proprietà è nota come voce di proprietà e corrisponde a un attributo definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="35b94-109">A property is known as a property entry and corresponds to an attribute defined in the schema.</span></span> <span data-ttu-id="35b94-110">Una voce di proprietà può contenere uno o molti valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="35b94-110">A property entry can have one, or many, property values.</span></span> <span data-ttu-id="35b94-111">Un set di voci di proprietà è organizzato come elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="35b94-111">A set of property entries are organized as a property list.</span></span>

<span data-ttu-id="35b94-112">L'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gestisce l'elenco delle proprietà di un oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="35b94-112">The [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface manages the property list of an ADSI object.</span></span> <span data-ttu-id="35b94-113">L'interfaccia [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) esegue questa operazione per una voce di proprietà.</span><span class="sxs-lookup"><span data-stu-id="35b94-113">The [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface performs this operation for a property entry.</span></span> <span data-ttu-id="35b94-114">Analogamente, l'interfaccia [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) rappresenta uno o più valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="35b94-114">Similarly, the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface represents one, or more, property values.</span></span> <span data-ttu-id="35b94-115">Insieme, forniscono un meccanismo per consentire agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="35b94-115">Together, they provide a mechanism for users to:</span></span>

-   <span data-ttu-id="35b94-116">Lavorare direttamente con la cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="35b94-116">Work directly with the property cache.</span></span>
-   <span data-ttu-id="35b94-117">Utilizzare le directory che non contengono schemi, ad esempio un server LDAP versione 2.</span><span class="sxs-lookup"><span data-stu-id="35b94-117">Work with directories that do not contain schemas, such as an LDAP version 2 server.</span></span>

<span data-ttu-id="35b94-118">Le interfacce [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* operano esclusivamente nella cache delle proprietà e non eseguono alcun tentativo di collaborazione con il server per recuperare o modificare i dati nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="35b94-118">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)\* interfaces operate strictly on the property cache and do not make any attempt to cooperate with the server to retrieve or modify the data in the persistent store.</span></span> <span data-ttu-id="35b94-119">Queste interfacce vengono usate solo per esaminare e modificare le proprietà nella cache del client.</span><span class="sxs-lookup"><span data-stu-id="35b94-119">As such, these interfaces are used only to examine and manipulate properties in the client cache.</span></span> <span data-ttu-id="35b94-120">Prima di usare queste interfacce, è necessario chiamare il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o il metodo [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) in modo esplicito per caricare le proprietà dell'oggetto nella cache, se la cache non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="35b94-120">Before using these interfaces, you must call the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method or the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method explicitly to load the object properties into the cache, if the cache has not been initialized.</span></span> <span data-ttu-id="35b94-121">Dopo la chiamata dei metodi di queste interfacce, è necessario chiamare [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per salvare in modo permanente le modifiche apportate all'archivio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="35b94-121">After calling the methods of these interfaces, you must call [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) to persist the changes to the underlying directory store.</span></span>

<span data-ttu-id="35b94-122">Per altre informazioni e un esempio di codice che può essere usato per implementare queste interfacce, vedere [il codice di esempio per l'uso delle interfacce IADsProperty per accedere alla cache delle proprietà](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span><span class="sxs-lookup"><span data-stu-id="35b94-122">For more information and a code example that can used to implement these interfaces, see [Example Code for Using IADsProperty Interfaces to Access the Property Cache](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span></span>

 

 




