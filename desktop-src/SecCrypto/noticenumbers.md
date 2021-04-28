---
description: 'Oggetto NoticeNumbers: rappresenta una raccolta di oggetti Extension.'
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
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090759"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="5a0d5-103">Oggetto NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="5a0d5-103">NoticeNumbers object</span></span>

<span data-ttu-id="5a0d5-104">\[**L'oggetto NoticeNumbers** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5a0d5-105">Per altre informazioni, vedere [**Qualificatore.**](qualifier.md)\]</span><span class="sxs-lookup"><span data-stu-id="5a0d5-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="5a0d5-106">**L'oggetto NoticeNumbers** rappresenta una raccolta di [**oggetti Extension.**](extension.md)</span><span class="sxs-lookup"><span data-stu-id="5a0d5-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="5a0d5-107">Ogni [**oggetto Extension**](extension.md) rappresenta un numero di avviso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5a0d5-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5a0d5-108">When to use</span></span>

<span data-ttu-id="5a0d5-109">**L'oggetto NoticeNumbers** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a0d5-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5a0d5-110">Recupera il numero di [**oggetti Extension**](extension.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="5a0d5-111">Recuperare un oggetto [**Extension**](extension.md) specifico dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="5a0d5-112">Scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="5a0d5-113">Membri</span><span class="sxs-lookup"><span data-stu-id="5a0d5-113">Members</span></span>

<span data-ttu-id="5a0d5-114">**L'oggetto NoticeNumbers** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a0d5-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="5a0d5-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a0d5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a0d5-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a0d5-116">Properties</span></span>

<span data-ttu-id="5a0d5-117">**L'oggetto NoticeNumbers** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="5a0d5-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a0d5-118">Property</span></span>                                              | <span data-ttu-id="5a0d5-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="5a0d5-119">Access type</span></span>          | <span data-ttu-id="5a0d5-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a0d5-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a0d5-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5a0d5-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="5a0d5-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a0d5-122">Read-only</span></span><br/> | <span data-ttu-id="5a0d5-123">Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="5a0d5-124">Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="5a0d5-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="5a0d5-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="5a0d5-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="5a0d5-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a0d5-126">Read-only</span></span><br/> | <span data-ttu-id="5a0d5-127">Recupera il numero di [**oggetti Extension**](extension.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="5a0d5-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5a0d5-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="5a0d5-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a0d5-129">Read-only</span></span><br/> | <span data-ttu-id="5a0d5-130">Recupera [**l'oggetto Extension**](extension.md) che rappresenta il numero di avviso indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="5a0d5-131">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5a0d5-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a0d5-132">Remarks</span></span>

<span data-ttu-id="5a0d5-133">Impossibile **creare l'oggetto NoticeNumbers.**</span><span class="sxs-lookup"><span data-stu-id="5a0d5-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="5a0d5-134">L'oggetto NoticeNumbers viene usato nella [**proprietà Qualifier.NoticeNumbers.**](qualifier-noticenumbers.md)</span><span class="sxs-lookup"><span data-stu-id="5a0d5-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0d5-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a0d5-135">Requirements</span></span>



| <span data-ttu-id="5a0d5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a0d5-136">Requirement</span></span> | <span data-ttu-id="5a0d5-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5a0d5-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0d5-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5a0d5-138">Redistributable</span></span><br/> | <span data-ttu-id="5a0d5-139">CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a0d5-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5a0d5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5a0d5-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="5a0d5-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a0d5-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
