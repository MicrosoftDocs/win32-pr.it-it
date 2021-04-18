---
description: Recupera il numero di versione principale del modello.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Proprietà Template. MajorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330602"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="14466-103">Proprietà Template. MajorVersion</span><span class="sxs-lookup"><span data-stu-id="14466-103">Template.MajorVersion property</span></span>

<span data-ttu-id="14466-104">\[La proprietà **MajorVersion** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="14466-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14466-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="14466-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="14466-106">La proprietà **MajorVersion** Recupera il numero di versione principale del modello.</span><span class="sxs-lookup"><span data-stu-id="14466-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="14466-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14466-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="14466-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="14466-108">Property value</span></span>

<span data-ttu-id="14466-109">Numero di versione principale del modello.</span><span class="sxs-lookup"><span data-stu-id="14466-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="14466-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14466-110">Requirements</span></span>



| <span data-ttu-id="14466-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="14466-111">Requirement</span></span> | <span data-ttu-id="14466-112">Valore</span><span class="sxs-lookup"><span data-stu-id="14466-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14466-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="14466-113">Redistributable</span></span><br/> | <span data-ttu-id="14466-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="14466-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14466-115">DLL</span><span class="sxs-lookup"><span data-stu-id="14466-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="14466-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14466-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14466-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14466-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14466-118">**Modello**</span><span class="sxs-lookup"><span data-stu-id="14466-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
