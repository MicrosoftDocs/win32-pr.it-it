---
description: Rappresenta l'estensione dei vincoli di base di un certificato.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Oggetto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331306"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="a79c3-103">Oggetto BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="a79c3-103">BasicConstraints object</span></span>

<span data-ttu-id="a79c3-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a79c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a79c3-105">Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="a79c3-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="a79c3-106">L'oggetto **BasicConstraints** rappresenta l'estensione dei vincoli di base di un certificato.</span><span class="sxs-lookup"><span data-stu-id="a79c3-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a79c3-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a79c3-107">When to use</span></span>

<span data-ttu-id="a79c3-108">L'oggetto **BasicConstraints** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="a79c3-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a79c3-109">Determinare se è presente l'estensione dei vincoli di base.</span><span class="sxs-lookup"><span data-stu-id="a79c3-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="a79c3-110">Determinare se l'estensione dei vincoli di base è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="a79c3-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="a79c3-111">Determinare se il certificato è vincolato alle autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="a79c3-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="a79c3-112">Determinare se il vincolo di lunghezza del percorso è presente e recuperare il valore del vincolo di lunghezza del percorso.</span><span class="sxs-lookup"><span data-stu-id="a79c3-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="a79c3-113">Membri</span><span class="sxs-lookup"><span data-stu-id="a79c3-113">Members</span></span>

<span data-ttu-id="a79c3-114">L'oggetto **BasicConstraints** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a79c3-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="a79c3-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a79c3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a79c3-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a79c3-116">Properties</span></span>

<span data-ttu-id="a79c3-117">L'oggetto **BasicConstraints** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a79c3-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="a79c3-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a79c3-118">Property</span></span>                                                                                     | <span data-ttu-id="a79c3-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a79c3-119">Access type</span></span>          | <span data-ttu-id="a79c3-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a79c3-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a79c3-121">**IsCertificateAuthority**</span><span class="sxs-lookup"><span data-stu-id="a79c3-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="a79c3-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a79c3-122">Read-only</span></span><br/> | <span data-ttu-id="a79c3-123">Recupera un valore booleano che indica se il certificato è per un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="a79c3-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="a79c3-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="a79c3-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="a79c3-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a79c3-125">Read-only</span></span><br/> | <span data-ttu-id="a79c3-126">Recupera un valore booleano che indica se l'estensione di vincolo di base è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="a79c3-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a79c3-127">**IsPathLenConstraintPresent**</span><span class="sxs-lookup"><span data-stu-id="a79c3-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="a79c3-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a79c3-128">Read-only</span></span><br/> | <span data-ttu-id="a79c3-129">Recupera un valore booleano che indica se è presente il vincolo di lunghezza del percorso del certificato.</span><span class="sxs-lookup"><span data-stu-id="a79c3-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a79c3-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="a79c3-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="a79c3-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a79c3-131">Read-only</span></span><br/> | <span data-ttu-id="a79c3-132">Recupera un valore booleano che indica se l'estensione dei vincoli di base è presente.</span><span class="sxs-lookup"><span data-stu-id="a79c3-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="a79c3-133">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="a79c3-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="a79c3-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="a79c3-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="a79c3-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a79c3-135">Read-only</span></span><br/> | <span data-ttu-id="a79c3-136">Recupera il valore del vincolo di lunghezza del percorso.</span><span class="sxs-lookup"><span data-stu-id="a79c3-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a79c3-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a79c3-137">Remarks</span></span>

<span data-ttu-id="a79c3-138">Impossibile creare l'oggetto **BasicConstraints** .</span><span class="sxs-lookup"><span data-stu-id="a79c3-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a79c3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a79c3-139">Requirements</span></span>



| <span data-ttu-id="a79c3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a79c3-140">Requirement</span></span> | <span data-ttu-id="a79c3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a79c3-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a79c3-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a79c3-142">End of client support</span></span><br/> | <span data-ttu-id="a79c3-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a79c3-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a79c3-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a79c3-144">End of server support</span></span><br/> | <span data-ttu-id="a79c3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a79c3-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a79c3-146">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a79c3-146">Redistributable</span></span><br/>       | <span data-ttu-id="a79c3-147">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a79c3-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a79c3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a79c3-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a79c3-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a79c3-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a79c3-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a79c3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79c3-151">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="a79c3-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
