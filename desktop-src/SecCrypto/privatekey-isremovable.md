---
description: Restituisce un valore booleano che indica se la chiave privata è nell'archivio rimovibile.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: Metodo PrivateKey. rimovibile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330604"
---
# <a name="privatekeyisremovable-method"></a><span data-ttu-id="cad76-103">Metodo PrivateKey. rimovibile</span><span class="sxs-lookup"><span data-stu-id="cad76-103">PrivateKey.IsRemovable method</span></span>

<span data-ttu-id="cad76-104">\[Il metodo **rimovibile** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="cad76-104">\[The **IsRemovable** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cad76-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cad76-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cad76-106">Il metodo **rimovibile** restituisce un valore booleano che indica se la chiave privata è in archivi rimovibili.</span><span class="sxs-lookup"><span data-stu-id="cad76-106">The **IsRemovable** method returns a Boolean value that indicates whether the private key is in removable storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad76-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cad76-107">Syntax</span></span>


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a><span data-ttu-id="cad76-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cad76-108">Parameters</span></span>

<span data-ttu-id="cad76-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cad76-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cad76-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cad76-110">Return value</span></span>

<span data-ttu-id="cad76-111">Se true, la chiave privata si trova in una risorsa di archiviazione rimovibile.</span><span class="sxs-lookup"><span data-stu-id="cad76-111">If true, the private key is in removable storage.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad76-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cad76-112">Remarks</span></span>

<span data-ttu-id="cad76-113">Il valore restituito di questo metodo dipende dal provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cad76-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="cad76-114">Questo metodo restituirà un valore attendibile se viene utilizzato un CSP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cad76-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="cad76-115">Se CSP non è un CSP Microsoft, il valore restituito non può essere considerato accurato.</span><span class="sxs-lookup"><span data-stu-id="cad76-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad76-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cad76-116">Requirements</span></span>



| <span data-ttu-id="cad76-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cad76-117">Requirement</span></span> | <span data-ttu-id="cad76-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cad76-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad76-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cad76-119">Redistributable</span></span><br/> | <span data-ttu-id="cad76-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cad76-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cad76-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cad76-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="cad76-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad76-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad76-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cad76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad76-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="cad76-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
