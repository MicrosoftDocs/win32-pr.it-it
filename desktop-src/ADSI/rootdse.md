---
title: RootDSE (ADSI)
description: Ogni server di directory dispone di una voce univoca denominata RootDSE. Fornisce dati sul server, ad esempio le funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730242"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="3c336-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="3c336-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="3c336-105">Ogni server di directory dispone di una voce univoca denominata **RootDSE**.</span><span class="sxs-lookup"><span data-stu-id="3c336-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="3c336-106">Fornisce dati sul server, ad esempio le funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.</span><span class="sxs-lookup"><span data-stu-id="3c336-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="3c336-107">Ad esempio, per creare uno script, o un'applicazione, che può essere eseguito in qualsiasi ambiente di dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="3c336-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="3c336-108">È possibile specificare il nome distinto, il nome del server o il nome di dominio quando ci si connette a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c336-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="3c336-109">Se non si dispone di queste informazioni, è possibile utilizzare l'oggetto **RootDSE** per stabilire una connessione.</span><span class="sxs-lookup"><span data-stu-id="3c336-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="3c336-110">Nell'esempio di codice seguente viene modificata la descrizione del dominio in qualsiasi dominio.</span><span class="sxs-lookup"><span data-stu-id="3c336-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="3c336-111">Ottenendo l'attributo **defaultNamingContext** da **RootDSE**, è possibile eseguire l'associazione al dominio corrente. ad esempio, Fabrikam **defaultNamingContext** è DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="3c336-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="3c336-112">Per enumerare le proprietà di **RootDSE**, usare l'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) .</span><span class="sxs-lookup"><span data-stu-id="3c336-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="3c336-113">Non è possibile usare [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per questa attività.</span><span class="sxs-lookup"><span data-stu-id="3c336-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="3c336-114">Per ulteriori informazioni, vedere [binding senza server e RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="3c336-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 