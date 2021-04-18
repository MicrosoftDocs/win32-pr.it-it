---
description: Rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331605"
---
# <a name="eku-object"></a><span data-ttu-id="cb641-103">EKU (oggetto)</span><span class="sxs-lookup"><span data-stu-id="cb641-103">EKU object</span></span>

<span data-ttu-id="cb641-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb641-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cb641-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cb641-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cb641-106">L'oggetto **EKU** rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.</span><span class="sxs-lookup"><span data-stu-id="cb641-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="cb641-107">Membri</span><span class="sxs-lookup"><span data-stu-id="cb641-107">Members</span></span>

<span data-ttu-id="cb641-108">L'oggetto **EKU** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cb641-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="cb641-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb641-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb641-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb641-110">Properties</span></span>

<span data-ttu-id="cb641-111">L'oggetto **EKU** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb641-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="cb641-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb641-112">Property</span></span>                            | <span data-ttu-id="cb641-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="cb641-113">Access type</span></span>           | <span data-ttu-id="cb641-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb641-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb641-115">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cb641-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="cb641-116">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cb641-116">Read/write</span></span><br/> | <span data-ttu-id="cb641-117">Imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU.</span><span class="sxs-lookup"><span data-stu-id="cb641-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="cb641-118">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb641-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="cb641-119">**OID**</span><span class="sxs-lookup"><span data-stu-id="cb641-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="cb641-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="cb641-120">Read/write</span></span><br/> | <span data-ttu-id="cb641-121">Imposta o Recupera una stringa che contiene un valore stringa OID (EKU [*Object Identifier*](../secgloss/o-gly.md) ) come definito in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="cb641-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb641-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb641-122">Remarks</span></span>

<span data-ttu-id="cb641-123">L'oggetto **EKU** viene usato dalla raccolta e dalla proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb641-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="cb641-124">Raccolta [**EKU**](ekus.md)</span><span class="sxs-lookup"><span data-stu-id="cb641-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="cb641-125">[**CertificateStatus. EKU**](certificatestatus-eku.md) (proprietà)</span><span class="sxs-lookup"><span data-stu-id="cb641-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="cb641-126">Impossibile creare l'oggetto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="cb641-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb641-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb641-127">Requirements</span></span>



| <span data-ttu-id="cb641-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb641-128">Requirement</span></span> | <span data-ttu-id="cb641-129">Valore</span><span class="sxs-lookup"><span data-stu-id="cb641-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb641-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cb641-130">End of client support</span></span><br/> | <span data-ttu-id="cb641-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb641-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cb641-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cb641-132">End of server support</span></span><br/> | <span data-ttu-id="cb641-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb641-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cb641-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cb641-134">Redistributable</span></span><br/>       | <span data-ttu-id="cb641-135">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb641-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cb641-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cb641-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cb641-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb641-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
