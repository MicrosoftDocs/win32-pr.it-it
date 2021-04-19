---
description: Recupera il nome del provider del servizio di crittografia (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: Proprietà PrivateKey. ProviderName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332924"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="02b63-103">Proprietà PrivateKey. ProviderName</span><span class="sxs-lookup"><span data-stu-id="02b63-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="02b63-104">\[La proprietà **providerName** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="02b63-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="02b63-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="02b63-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="02b63-106">La proprietà **providerName** Recupera il nome del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="02b63-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="02b63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02b63-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="02b63-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="02b63-108">Property value</span></span>

<span data-ttu-id="02b63-109">Stringa che contiene il nome del CSP.</span><span class="sxs-lookup"><span data-stu-id="02b63-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b63-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02b63-110">Requirements</span></span>



| <span data-ttu-id="02b63-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="02b63-111">Requirement</span></span> | <span data-ttu-id="02b63-112">Valore</span><span class="sxs-lookup"><span data-stu-id="02b63-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02b63-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="02b63-113">Redistributable</span></span><br/> | <span data-ttu-id="02b63-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="02b63-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="02b63-115">DLL</span><span class="sxs-lookup"><span data-stu-id="02b63-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="02b63-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02b63-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b63-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02b63-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b63-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="02b63-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
