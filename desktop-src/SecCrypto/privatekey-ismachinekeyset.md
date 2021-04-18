---
description: Restituisce un valore booleano che indica se la chiave privata appartiene a un set di chiavi del computer.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. IsMachineKeyset, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333776"
---
# <a name="privatekeyismachinekeyset-method"></a><span data-ttu-id="39301-103">PrivateKey. IsMachineKeyset, metodo</span><span class="sxs-lookup"><span data-stu-id="39301-103">PrivateKey.IsMachineKeyset method</span></span>

<span data-ttu-id="39301-104">\[Il metodo **IsMachineKeyset** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="39301-104">\[The **IsMachineKeyset** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="39301-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="39301-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="39301-106">Il metodo **IsMachineKeyset** restituisce un valore booleano che indica se la chiave privata appartiene a un set di chiavi del computer.</span><span class="sxs-lookup"><span data-stu-id="39301-106">The **IsMachineKeyset** method returns a Boolean value that indicates whether the private key belongs to a machine key set.</span></span>

## <a name="syntax"></a><span data-ttu-id="39301-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39301-107">Syntax</span></span>


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a><span data-ttu-id="39301-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39301-108">Parameters</span></span>

<span data-ttu-id="39301-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="39301-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39301-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39301-110">Return value</span></span>

<span data-ttu-id="39301-111">Se true, la chiave privata appartiene a un set di chiavi del computer.</span><span class="sxs-lookup"><span data-stu-id="39301-111">If true, the private key belongs to a machine key set.</span></span>

## <a name="remarks"></a><span data-ttu-id="39301-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="39301-112">Remarks</span></span>

<span data-ttu-id="39301-113">Il valore restituito di questo metodo dipende dal provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzato.</span><span class="sxs-lookup"><span data-stu-id="39301-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="39301-114">Questo metodo restituirà un valore attendibile se viene utilizzato un CSP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39301-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="39301-115">Se CSP non è un CSP Microsoft, il valore restituito non può essere considerato accurato.</span><span class="sxs-lookup"><span data-stu-id="39301-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="39301-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39301-116">Requirements</span></span>



| <span data-ttu-id="39301-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39301-117">Requirement</span></span> | <span data-ttu-id="39301-118">Valore</span><span class="sxs-lookup"><span data-stu-id="39301-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39301-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="39301-119">Redistributable</span></span><br/> | <span data-ttu-id="39301-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="39301-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39301-121">DLL</span><span class="sxs-lookup"><span data-stu-id="39301-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="39301-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39301-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39301-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39301-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39301-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="39301-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
