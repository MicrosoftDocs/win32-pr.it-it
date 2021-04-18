---
description: Restituisce un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware.
ms.assetid: 9a06f598-55cd-441b-a85f-8bec299f8245
title: PrivateKey. IsHardwareDevice, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsHardwareDevice
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23b6fd379fd3a3b53fe0600dbf28481cd5ef2f86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333777"
---
# <a name="privatekeyishardwaredevice-method"></a><span data-ttu-id="7bf85-103">PrivateKey. IsHardwareDevice, metodo</span><span class="sxs-lookup"><span data-stu-id="7bf85-103">PrivateKey.IsHardwareDevice method</span></span>

<span data-ttu-id="7bf85-104">\[Il metodo **IsHardwareDevice** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7bf85-104">\[The **IsHardwareDevice** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7bf85-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7bf85-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7bf85-106">Il metodo **IsHardwareDevice** restituisce un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="7bf85-106">The **IsHardwareDevice** method returns a Boolean value that indicates whether the private key is stored in a hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf85-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bf85-107">Syntax</span></span>


```VB
PrivateKey.IsHardwareDevice()
```



## <a name="parameters"></a><span data-ttu-id="7bf85-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bf85-108">Parameters</span></span>

<span data-ttu-id="7bf85-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7bf85-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bf85-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bf85-110">Return value</span></span>

<span data-ttu-id="7bf85-111">Se true, la chiave privata viene archiviata in un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="7bf85-111">If true, the private key is stored in a hardware device.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf85-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bf85-112">Remarks</span></span>

<span data-ttu-id="7bf85-113">Il valore restituito di questo metodo dipende dal provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7bf85-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="7bf85-114">Questo metodo restituirà un valore attendibile se viene utilizzato un CSP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7bf85-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="7bf85-115">Se CSP non è un CSP Microsoft, il valore restituito non può essere considerato accurato.</span><span class="sxs-lookup"><span data-stu-id="7bf85-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf85-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bf85-116">Requirements</span></span>



| <span data-ttu-id="7bf85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf85-117">Requirement</span></span> | <span data-ttu-id="7bf85-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf85-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf85-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7bf85-119">Redistributable</span></span><br/> | <span data-ttu-id="7bf85-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bf85-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7bf85-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7bf85-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="7bf85-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bf85-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf85-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bf85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf85-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="7bf85-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
