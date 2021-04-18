---
description: Rappresenta una raccolta di oggetti di estensione.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Oggetto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332010"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="c55aa-103">Oggetto NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="c55aa-103">NoticeNumbers object</span></span>

<span data-ttu-id="c55aa-104">\[L'oggetto **NoticeNumbers** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c55aa-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c55aa-105">Per ulteriori informazioni, vedere [**qualificatore**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="c55aa-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="c55aa-106">L'oggetto **NoticeNumbers** rappresenta una raccolta di oggetti di [**estensione**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="c55aa-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="c55aa-107">Ogni oggetto [**estensione**](extension.md) rappresenta un numero di avviso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c55aa-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c55aa-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c55aa-108">When to use</span></span>

<span data-ttu-id="c55aa-109">L'oggetto **NoticeNumbers** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="c55aa-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c55aa-110">Recuperare il numero di oggetti [**estensione**](extension.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="c55aa-111">Recuperare un oggetto [**estensione**](extension.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="c55aa-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="c55aa-113">Membri</span><span class="sxs-lookup"><span data-stu-id="c55aa-113">Members</span></span>

<span data-ttu-id="c55aa-114">L'oggetto **NoticeNumbers** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c55aa-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="c55aa-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c55aa-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c55aa-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c55aa-116">Properties</span></span>

<span data-ttu-id="c55aa-117">L'oggetto **NoticeNumbers** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c55aa-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="c55aa-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c55aa-118">Property</span></span>                                              | <span data-ttu-id="c55aa-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c55aa-119">Access type</span></span>          | <span data-ttu-id="c55aa-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c55aa-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c55aa-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="c55aa-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="c55aa-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c55aa-122">Read-only</span></span><br/> | <span data-ttu-id="c55aa-123">Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c55aa-124">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c55aa-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="c55aa-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="c55aa-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="c55aa-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c55aa-126">Read-only</span></span><br/> | <span data-ttu-id="c55aa-127">Recupera il numero di oggetti di [**estensione**](extension.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="c55aa-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c55aa-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="c55aa-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c55aa-129">Read-only</span></span><br/> | <span data-ttu-id="c55aa-130">Recupera l'oggetto di [**estensione**](extension.md) che rappresenta il numero dell'avviso indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c55aa-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="c55aa-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="c55aa-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c55aa-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c55aa-132">Remarks</span></span>

<span data-ttu-id="c55aa-133">Impossibile creare l'oggetto **NoticeNumbers** .</span><span class="sxs-lookup"><span data-stu-id="c55aa-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="c55aa-134">L'oggetto NoticeNumbers viene usato nella proprietà [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="c55aa-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55aa-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c55aa-135">Requirements</span></span>



| <span data-ttu-id="c55aa-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55aa-136">Requirement</span></span> | <span data-ttu-id="c55aa-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c55aa-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55aa-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c55aa-138">Redistributable</span></span><br/> | <span data-ttu-id="c55aa-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="c55aa-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c55aa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c55aa-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="c55aa-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55aa-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
