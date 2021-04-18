---
description: Recupera il contenuto dell'avviso dell'utente.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Proprietà Qualifier. ExplicitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327089"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="14358-103">Proprietà Qualifier. ExplicitText</span><span class="sxs-lookup"><span data-stu-id="14358-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="14358-104">\[La proprietà **ExplicitText** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="14358-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14358-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="14358-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="14358-106">La proprietà **ExplicitText** Recupera il contenuto della comunicazione utente.</span><span class="sxs-lookup"><span data-stu-id="14358-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="14358-107">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="14358-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="14358-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14358-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="14358-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="14358-109">Property value</span></span>

<span data-ttu-id="14358-110">Contenuto dell'avviso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="14358-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="14358-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14358-111">Requirements</span></span>



| <span data-ttu-id="14358-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="14358-112">Requirement</span></span> | <span data-ttu-id="14358-113">Valore</span><span class="sxs-lookup"><span data-stu-id="14358-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14358-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="14358-114">Redistributable</span></span><br/> | <span data-ttu-id="14358-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="14358-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14358-116">DLL</span><span class="sxs-lookup"><span data-stu-id="14358-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="14358-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14358-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14358-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14358-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14358-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="14358-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
