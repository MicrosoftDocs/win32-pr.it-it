---
description: Recupera il nome del modello.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Proprietà Template.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330600"
---
# <a name="templatename-property"></a><span data-ttu-id="99b7f-103">Proprietà Template.Name</span><span class="sxs-lookup"><span data-stu-id="99b7f-103">Template.Name property</span></span>

<span data-ttu-id="99b7f-104">\[La proprietà **Name** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="99b7f-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="99b7f-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="99b7f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="99b7f-106">La proprietà **Name** Recupera il nome del modello.</span><span class="sxs-lookup"><span data-stu-id="99b7f-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b7f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99b7f-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="99b7f-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="99b7f-108">Property value</span></span>

<span data-ttu-id="99b7f-109">Nome del modello.</span><span class="sxs-lookup"><span data-stu-id="99b7f-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b7f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99b7f-110">Requirements</span></span>



| <span data-ttu-id="99b7f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b7f-111">Requirement</span></span> | <span data-ttu-id="99b7f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="99b7f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b7f-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="99b7f-113">Redistributable</span></span><br/> | <span data-ttu-id="99b7f-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="99b7f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="99b7f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="99b7f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="99b7f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b7f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b7f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99b7f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b7f-118">**Modello**</span><span class="sxs-lookup"><span data-stu-id="99b7f-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
