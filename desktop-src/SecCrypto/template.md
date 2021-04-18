---
description: Rappresenta il modello di estensione del certificato del certificato.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Oggetto modello
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330596"
---
# <a name="template-object"></a><span data-ttu-id="20592-103">Oggetto modello</span><span class="sxs-lookup"><span data-stu-id="20592-103">Template object</span></span>

<span data-ttu-id="20592-104">\[L'oggetto **modello** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="20592-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20592-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="20592-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="20592-106">L'oggetto **modello** rappresenta il modello di estensione del certificato del certificato.</span><span class="sxs-lookup"><span data-stu-id="20592-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="20592-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="20592-107">When to use</span></span>

<span data-ttu-id="20592-108">L'oggetto **modello** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="20592-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="20592-109">Determinare se il modello è contrassegnato come critico o presente.</span><span class="sxs-lookup"><span data-stu-id="20592-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="20592-110">Recuperare l' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) o il nome del modello.</span><span class="sxs-lookup"><span data-stu-id="20592-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="20592-111">Recuperare la versione secondaria o principale del modello.</span><span class="sxs-lookup"><span data-stu-id="20592-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="20592-112">Membri</span><span class="sxs-lookup"><span data-stu-id="20592-112">Members</span></span>

<span data-ttu-id="20592-113">L'oggetto **modello** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20592-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="20592-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20592-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20592-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20592-115">Properties</span></span>

<span data-ttu-id="20592-116">L'oggetto **modello** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="20592-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="20592-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20592-117">Property</span></span>                                                 | <span data-ttu-id="20592-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="20592-118">Access type</span></span>          | <span data-ttu-id="20592-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20592-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20592-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="20592-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="20592-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-121">Read-only</span></span><br/> | <span data-ttu-id="20592-122">Recupera un valore booleano che indica se l'estensione del modello è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="20592-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="20592-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="20592-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="20592-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-124">Read-only</span></span><br/> | <span data-ttu-id="20592-125">Recupera un valore booleano che indica se l'estensione del modello è presente.</span><span class="sxs-lookup"><span data-stu-id="20592-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="20592-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="20592-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="20592-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-127">Read-only</span></span><br/> | <span data-ttu-id="20592-128">Recupera il numero di versione principale del modello.</span><span class="sxs-lookup"><span data-stu-id="20592-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="20592-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="20592-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="20592-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-130">Read-only</span></span><br/> | <span data-ttu-id="20592-131">Recupera il numero di versione secondario del modello.</span><span class="sxs-lookup"><span data-stu-id="20592-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="20592-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20592-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="20592-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-133">Read-only</span></span><br/> | <span data-ttu-id="20592-134">Recupera una stringa che contiene il nome del modello.</span><span class="sxs-lookup"><span data-stu-id="20592-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="20592-135">**OID**</span><span class="sxs-lookup"><span data-stu-id="20592-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="20592-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="20592-136">Read-only</span></span><br/> | <span data-ttu-id="20592-137">Recupera un oggetto [**OID**](oid.md) che identifica l'oggetto **modello** .</span><span class="sxs-lookup"><span data-stu-id="20592-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="20592-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="20592-138">Remarks</span></span>

<span data-ttu-id="20592-139">Impossibile creare l'oggetto **modello** .</span><span class="sxs-lookup"><span data-stu-id="20592-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="20592-140">Un oggetto **modello** viene restituito dal metodo [**Certificate. template**](certificate-template.md) .</span><span class="sxs-lookup"><span data-stu-id="20592-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="20592-141">CAPICOM usa due versioni diverse dei modelli di certificato.</span><span class="sxs-lookup"><span data-stu-id="20592-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="20592-142">La tabella seguente mostra il nome e l'OID per ogni versione del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="20592-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="20592-143">Versione</span><span class="sxs-lookup"><span data-stu-id="20592-143">Version</span></span> | <span data-ttu-id="20592-144">Nome</span><span class="sxs-lookup"><span data-stu-id="20592-144">Name</span></span>                               | <span data-ttu-id="20592-145">OID</span><span class="sxs-lookup"><span data-stu-id="20592-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="20592-146">V1</span><span class="sxs-lookup"><span data-stu-id="20592-146">V1</span></span>      | <span data-ttu-id="20592-147">szOID \_ registrazione \_ \_ estensione tipo certificato</span><span class="sxs-lookup"><span data-stu-id="20592-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="20592-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="20592-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="20592-149">V2</span><span class="sxs-lookup"><span data-stu-id="20592-149">V2</span></span>      | <span data-ttu-id="20592-150">\_modello di certificato szOID \_</span><span class="sxs-lookup"><span data-stu-id="20592-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="20592-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="20592-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="20592-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20592-152">Requirements</span></span>



| <span data-ttu-id="20592-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="20592-153">Requirement</span></span> | <span data-ttu-id="20592-154">Valore</span><span class="sxs-lookup"><span data-stu-id="20592-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20592-155">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="20592-155">Redistributable</span></span><br/> | <span data-ttu-id="20592-156">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="20592-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20592-157">DLL</span><span class="sxs-lookup"><span data-stu-id="20592-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="20592-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20592-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
