---
title: Utilizzo di un oggetto dati ActiveX per l'associazione a provider ADSI
description: Poiché ADSI è anche un provider di OLE DB, è possibile utilizzare un oggetto ADO (ActiveX Data Object) per connettersi ai provider ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX Data Object ADSI
- ActiveX Data Object ADSI, utilizzo di ADO per l'associazione a provider ADSI
- provider di servizi ADSI, utilizzo dell'oggetto dati ActiveX per l'associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044047"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="eb2ac-106">Utilizzo di un oggetto dati ActiveX per l'associazione a provider ADSI</span><span class="sxs-lookup"><span data-stu-id="eb2ac-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="eb2ac-107">Poiché ADSI è anche un provider di OLE DB, è possibile utilizzare un oggetto ADO (ActiveX Data Object) per connettersi ai provider ADSI.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="eb2ac-108">Come per gli altri provider ADO, per connettersi a un provider di OLE DB, è necessario creare un nuovo oggetto connessione e, facoltativamente, specificare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="eb2ac-109">Il nome del provider OLE DB ADSI è **ADSDSOObject**.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="eb2ac-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="eb2ac-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="eb2ac-111">Nell'esempio precedente si è connessi per conto dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="eb2ac-112">Per specificare credenziali diverse, utilizzare le proprietà di connessione:</span><span class="sxs-lookup"><span data-stu-id="eb2ac-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="eb2ac-113">ADSI OLE DB definisce le proprietà di connessione seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="eb2ac-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb2ac-114">Property</span></span>           | <span data-ttu-id="eb2ac-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eb2ac-115">Data type</span></span>   | <span data-ttu-id="eb2ac-116">Predefinito</span><span class="sxs-lookup"><span data-stu-id="eb2ac-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="eb2ac-117">"User ID"</span><span class="sxs-lookup"><span data-stu-id="eb2ac-117">"User ID"</span></span>          | <span data-ttu-id="eb2ac-118">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-118">**BSTR**</span></span>    | <span data-ttu-id="eb2ac-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-119">**NULL**</span></span>  |
| <span data-ttu-id="eb2ac-120">"Password"</span><span class="sxs-lookup"><span data-stu-id="eb2ac-120">"Password"</span></span>         | <span data-ttu-id="eb2ac-121">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-121">**BSTR**</span></span>    | <span data-ttu-id="eb2ac-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-122">**NULL**</span></span>  |
| <span data-ttu-id="eb2ac-123">"Crittografa password"</span><span class="sxs-lookup"><span data-stu-id="eb2ac-123">"Encrypt Password"</span></span> | <span data-ttu-id="eb2ac-124">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-124">**BOOLEAN**</span></span> | <span data-ttu-id="eb2ac-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-125">**FALSE**</span></span> |
| <span data-ttu-id="eb2ac-126">"Flag ADSI"</span><span class="sxs-lookup"><span data-stu-id="eb2ac-126">"ADSI Flag"</span></span>        | <span data-ttu-id="eb2ac-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="eb2ac-127">**Long**</span></span>    | <span data-ttu-id="eb2ac-128">0</span><span class="sxs-lookup"><span data-stu-id="eb2ac-128">0</span></span>         |



 

<span data-ttu-id="eb2ac-129">Utilizzando OLE DB ADO, non è possibile eseguire l'associazione a un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="eb2ac-130">È tuttavia possibile eseguire una query su un oggetto specifico e ottenere un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="eb2ac-131">Solo i provider ADSI che supportano [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) traggono vantaggio da ADO come modello di programmazione.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="eb2ac-132">La proprietà del flag ADSI viene utilizzata per specificare l'opzione di autenticazione del binding.</span><span class="sxs-lookup"><span data-stu-id="eb2ac-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="eb2ac-133">Questa proprietà può essere una combinazione di flag dell'enumerazione dell'enumerazione di [**\_ \_ autenticazione ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .</span><span class="sxs-lookup"><span data-stu-id="eb2ac-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




