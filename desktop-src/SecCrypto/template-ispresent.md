---
description: Recupera un valore booleano che indica se l'estensione del modello è presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Proprietà Template. Presenter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324593"
---
# <a name="templateispresent-property"></a><span data-ttu-id="aa63b-103">Proprietà Template. Presenter</span><span class="sxs-lookup"><span data-stu-id="aa63b-103">Template.IsPresent property</span></span>

<span data-ttu-id="aa63b-104">\[La proprietà **impresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="aa63b-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aa63b-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="aa63b-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="aa63b-106">La proprietà **impresent** recupera un valore booleano che indica se l'estensione del modello è presente.</span><span class="sxs-lookup"><span data-stu-id="aa63b-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa63b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa63b-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="aa63b-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aa63b-108">Property value</span></span>

<span data-ttu-id="aa63b-109">Se **true**, è presente l'estensione del modello.</span><span class="sxs-lookup"><span data-stu-id="aa63b-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa63b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa63b-110">Requirements</span></span>



| <span data-ttu-id="aa63b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa63b-111">Requirement</span></span> | <span data-ttu-id="aa63b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aa63b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa63b-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="aa63b-113">Redistributable</span></span><br/> | <span data-ttu-id="aa63b-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa63b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aa63b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="aa63b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="aa63b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa63b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa63b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa63b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa63b-118">**Modello**</span><span class="sxs-lookup"><span data-stu-id="aa63b-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
