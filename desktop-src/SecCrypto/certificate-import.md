---
description: Importa un certificato codificato in precedenza da una stringa nell'oggetto certificato.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'Metodo ICertificate2:: Import'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326362"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="4cbd2-103">Metodo ICertificate2:: Import</span><span class="sxs-lookup"><span data-stu-id="4cbd2-103">ICertificate2::Import method</span></span>

<span data-ttu-id="4cbd2-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4cbd2-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4cbd2-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4cbd2-106">Il metodo **Import** importa un certificato codificato in precedenza da una stringa nell'oggetto [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbd2-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="4cbd2-107">La chiamata a questo metodo reimposta lo [*stato*](../secgloss/s-gly.md) di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbd2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cbd2-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="4cbd2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cbd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cbd2-110">*EncodedCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cbd2-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbd2-111">Stringa che contiene i dati del certificato codificato da importare.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cbd2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cbd2-112">Return value</span></span>

<span data-ttu-id="4cbd2-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cbd2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cbd2-114">Requirements</span></span>



| <span data-ttu-id="4cbd2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cbd2-115">Requirement</span></span> | <span data-ttu-id="4cbd2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4cbd2-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbd2-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4cbd2-117">End of client support</span></span><br/> | <span data-ttu-id="4cbd2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cbd2-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4cbd2-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4cbd2-119">End of server support</span></span><br/> | <span data-ttu-id="4cbd2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cbd2-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4cbd2-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4cbd2-121">Redistributable</span></span><br/>       | <span data-ttu-id="4cbd2-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4cbd2-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4cbd2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4cbd2-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4cbd2-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cbd2-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cbd2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cbd2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cbd2-126">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="4cbd2-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4cbd2-127">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
