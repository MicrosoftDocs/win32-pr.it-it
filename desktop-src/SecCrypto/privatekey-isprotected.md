---
description: Restituisce un valore booleano che indica se la chiave privata è protetta.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: Metodo PrivateKey. protected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330607"
---
# <a name="privatekeyisprotected-method"></a><span data-ttu-id="e9cb6-103">Metodo PrivateKey. protected</span><span class="sxs-lookup"><span data-stu-id="e9cb6-103">PrivateKey.IsProtected method</span></span>

<span data-ttu-id="e9cb6-104">\[Il metodo **protetto** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-104">\[The **IsProtected** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9cb6-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e9cb6-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e9cb6-106">Il **metodo protetto** restituisce un valore booleano che indica se la chiave privata è protetta.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-106">The **IsProtected** method returns a Boolean value that indicates whether the private key is protected.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cb6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9cb6-107">Syntax</span></span>


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a><span data-ttu-id="e9cb6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9cb6-108">Parameters</span></span>

<span data-ttu-id="e9cb6-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9cb6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9cb6-110">Return value</span></span>

<span data-ttu-id="e9cb6-111">Se true, la chiave privata è protetta.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-111">If true, the private key is protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9cb6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9cb6-112">Remarks</span></span>

<span data-ttu-id="e9cb6-113">Il valore restituito di questo metodo dipende dal provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="e9cb6-114">Questo metodo restituirà un valore attendibile se viene utilizzato un CSP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="e9cb6-115">Se CSP non è un CSP Microsoft, il valore restituito non può essere considerato accurato.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cb6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9cb6-116">Requirements</span></span>



| <span data-ttu-id="e9cb6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9cb6-117">Requirement</span></span> | <span data-ttu-id="e9cb6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e9cb6-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cb6-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e9cb6-119">Redistributable</span></span><br/> | <span data-ttu-id="e9cb6-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9cb6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e9cb6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e9cb6-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="e9cb6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9cb6-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cb6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9cb6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cb6-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
