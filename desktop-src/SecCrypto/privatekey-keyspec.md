---
description: Recupera la specifica della chiave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: Proprietà PrivateKey. dataspec
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330603"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="526e6-103">Proprietà PrivateKey. dataspec</span><span class="sxs-lookup"><span data-stu-id="526e6-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="526e6-104">\[La proprietà di una **specifica** di parametro è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="526e6-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="526e6-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="526e6-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="526e6-106">La **proprietà chiave specifica recupera** la specifica della chiave.</span><span class="sxs-lookup"><span data-stu-id="526e6-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="526e6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="526e6-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="526e6-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="526e6-108">Property value</span></span>

<span data-ttu-id="526e6-109">Valore dell'enumerazione delle [**\_ \_ specifiche della chiave capicot**](capicom-key-spec.md) che indica la specifica della chiave.</span><span class="sxs-lookup"><span data-stu-id="526e6-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="526e6-110">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="526e6-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="526e6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="526e6-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="526e6-112">Significato</span><span class="sxs-lookup"><span data-stu-id="526e6-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="526e6-113"><dt>**chiave per lo \_ scambio di chiavi di CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="526e6-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="526e6-114">La chiave può essere usata per la crittografia e la firma.</span><span class="sxs-lookup"><span data-stu-id="526e6-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="526e6-115"><dt>**firma della specifica della \_ chiave CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="526e6-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="526e6-116">La chiave può essere usata solo per la firma.</span><span class="sxs-lookup"><span data-stu-id="526e6-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="526e6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="526e6-117">Requirements</span></span>



| <span data-ttu-id="526e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="526e6-118">Requirement</span></span> | <span data-ttu-id="526e6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="526e6-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="526e6-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="526e6-120">Redistributable</span></span><br/> | <span data-ttu-id="526e6-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="526e6-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="526e6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="526e6-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="526e6-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="526e6-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="526e6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="526e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526e6-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="526e6-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
