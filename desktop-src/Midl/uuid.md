---
title: uuid (attributo)
description: L'attributo \ UUID \ Interface definisce un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue dalle altre interfacce.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- attributo uuid attributo MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718535"
---
# <a name="uuid-attribute"></a><span data-ttu-id="be390-104">uuid (attributo)</span><span class="sxs-lookup"><span data-stu-id="be390-104">uuid attribute</span></span>

<span data-ttu-id="be390-105">L'attributo di interfaccia **\[ UUID \]** designa un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue dalle altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="be390-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="be390-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be390-107">*stringa-UUID*</span><span class="sxs-lookup"><span data-stu-id="be390-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="be390-108">Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi da tre gruppi di 4 cifre esadecimali seguite da un trattino e quindi da 12 cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="be390-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="be390-109">È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="be390-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be390-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="be390-110">Remarks</span></span>

<span data-ttu-id="be390-111">La libreria di runtime utilizza l'UUID dell'interfaccia che l'attributo **\[ UUID \]** designa per stabilire la comunicazione tra le applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="be390-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="be390-112">L'attributo **\[ UUID \]** può essere visualizzato nell'elenco di attributi di interfaccia per un'interfaccia RPC o un'interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="be390-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="be390-113">Per un'interfaccia RPC, è necessario che l'elenco di attributi di interfaccia includa l'attributo **\[ UUID \]** o l' **\[** attributo [**local**](local.md) e che quello scelto venga **\]** eseguito esattamente una volta.</span><span class="sxs-lookup"><span data-stu-id="be390-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="be390-114">Se l'elenco include l'attributo **\[ UUID \]** , può includere anche l'attributo **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="be390-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="be390-115">Per un'interfaccia COM (identificata dall' **\[** [](object.md) **\]** attributo dell'interfaccia oggetto), l'elenco di attributi di interfaccia deve includere l'attributo **\[ UUID \]** , ma non può includere l'attributo **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="be390-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="be390-116">L'elenco di un'interfaccia COM può includere l'attributo **\[ locale \]** anche se è presente l'attributo **\[ UUID \]** .</span><span class="sxs-lookup"><span data-stu-id="be390-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="be390-117">Microsoft RPC supporta un'estensione di DCE IDL che consente di racchiudere l'UUID tra virgolette doppie ("" "").</span><span class="sxs-lookup"><span data-stu-id="be390-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="be390-118">Il formato racchiuso tra virgolette è necessario per i preprocessori del compilatore C che interpretano i numeri UUID come numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="be390-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="be390-119">Tutti i valori UUID devono essere generati dal computer per garantire l'univocità.</span><span class="sxs-lookup"><span data-stu-id="be390-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="be390-120">Usare l'utilità uuidgen per generare valori UUID univoci.</span><span class="sxs-lookup"><span data-stu-id="be390-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="be390-121">I numeri di versione e UUID dell'interfaccia vengono usati per determinare se il client può essere associato al server.</span><span class="sxs-lookup"><span data-stu-id="be390-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="be390-122">Affinché il client venga associato al server, l'UUID specificato nelle interfacce client e server deve essere lo stesso.</span><span class="sxs-lookup"><span data-stu-id="be390-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="be390-123">Si noti che un'interfaccia senza attributi può essere importata in un file IDL di base.</span><span class="sxs-lookup"><span data-stu-id="be390-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="be390-124">Tuttavia, l'interfaccia deve contenere solo tipi di oggetto senza procedure.</span><span class="sxs-lookup"><span data-stu-id="be390-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="be390-125">Se nell'interfaccia è inclusa anche una routine, è necessario specificare un attributo local o UUID.</span><span class="sxs-lookup"><span data-stu-id="be390-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="be390-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="be390-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="be390-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="be390-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be390-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="be390-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="be390-129">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="be390-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="be390-130">**locale**</span><span class="sxs-lookup"><span data-stu-id="be390-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="be390-131">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="be390-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="be390-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="be390-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="be390-133">**Versione**</span><span class="sxs-lookup"><span data-stu-id="be390-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




