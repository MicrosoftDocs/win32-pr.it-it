---
description: Rimuove un oggetto certificato da una raccolta di destinatari.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Recipients. Remove (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326349"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="ad98f-103">Recipients. Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="ad98f-103">Recipients.Remove method</span></span>

<span data-ttu-id="ad98f-104">\[Il metodo **Remove** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ad98f-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ad98f-105">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ad98f-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ad98f-106">Il metodo **Remove** rimuove un oggetto [**certificato**](certificate.md) da una raccolta [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="ad98f-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad98f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad98f-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="ad98f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad98f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad98f-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ad98f-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad98f-110">Indice dell'oggetto [**certificato**](certificate.md) da rimuovere dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad98f-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad98f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad98f-111">Return value</span></span>

<span data-ttu-id="ad98f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ad98f-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad98f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad98f-113">Requirements</span></span>



| <span data-ttu-id="ad98f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad98f-114">Requirement</span></span> | <span data-ttu-id="ad98f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ad98f-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad98f-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ad98f-116">Redistributable</span></span><br/> | <span data-ttu-id="ad98f-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad98f-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ad98f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ad98f-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="ad98f-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad98f-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad98f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad98f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad98f-121">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="ad98f-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ad98f-122">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="ad98f-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
