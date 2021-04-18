---
description: Recupera i parametri dell'algoritmo a chiave pubblica.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Proprietà PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329329"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="48a48-103">Proprietà PublicKey. EncodedParameters</span><span class="sxs-lookup"><span data-stu-id="48a48-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="48a48-104">\[La proprietà **EncodedParameters** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="48a48-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="48a48-105">Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="48a48-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="48a48-106">La proprietà **EncodedParameters** recupera i parametri dell'algoritmo a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="48a48-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48a48-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="48a48-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="48a48-108">Property value</span></span>

<span data-ttu-id="48a48-109">Oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso ai parametri dell'algoritmo a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="48a48-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a48-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a48-110">Requirements</span></span>



| <span data-ttu-id="48a48-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a48-111">Requirement</span></span> | <span data-ttu-id="48a48-112">Valore</span><span class="sxs-lookup"><span data-stu-id="48a48-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48a48-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="48a48-113">Redistributable</span></span><br/> | <span data-ttu-id="48a48-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="48a48-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="48a48-115">DLL</span><span class="sxs-lookup"><span data-stu-id="48a48-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="48a48-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a48-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a48-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48a48-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a48-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="48a48-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
