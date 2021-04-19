---
description: Recupera il nome dell'organizzazione associata al qualificatore.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Proprietà Qualifier. OrganizationName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329009"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="f93aa-103">Proprietà Qualifier. OrganizationName</span><span class="sxs-lookup"><span data-stu-id="f93aa-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="f93aa-104">\[La proprietà **OrganizationName** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f93aa-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f93aa-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="f93aa-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="f93aa-106">La proprietà **OrganizationName** Recupera il nome dell'organizzazione associata al qualificatore.</span><span class="sxs-lookup"><span data-stu-id="f93aa-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="f93aa-107">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="f93aa-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f93aa-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="f93aa-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f93aa-109">Property value</span></span>

<span data-ttu-id="f93aa-110">Nome dell'organizzazione associata al qualificatore.</span><span class="sxs-lookup"><span data-stu-id="f93aa-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="f93aa-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f93aa-111">Requirements</span></span>



| <span data-ttu-id="f93aa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f93aa-112">Requirement</span></span> | <span data-ttu-id="f93aa-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f93aa-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f93aa-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f93aa-114">Redistributable</span></span><br/> | <span data-ttu-id="f93aa-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f93aa-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f93aa-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f93aa-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="f93aa-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f93aa-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f93aa-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f93aa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f93aa-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="f93aa-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
