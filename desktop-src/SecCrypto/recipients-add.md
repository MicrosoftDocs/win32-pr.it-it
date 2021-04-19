---
description: Aggiunge un oggetto certificato a una raccolta di destinatari.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Metodo Recipients. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326356"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="5a14a-103">Metodo Recipients. Add</span><span class="sxs-lookup"><span data-stu-id="5a14a-103">Recipients.Add method</span></span>

<span data-ttu-id="5a14a-104">\[Il metodo **Add** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5a14a-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5a14a-105">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5a14a-106">Il metodo **Add** aggiunge un oggetto [**Certificate**](certificate.md) a una raccolta [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="5a14a-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a14a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a14a-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="5a14a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a14a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a14a-109">*Certificato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a14a-110">Espressione che viene risolta nell'oggetto [**certificato**](certificate.md) da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5a14a-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a14a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a14a-111">Return value</span></span>

<span data-ttu-id="5a14a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5a14a-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a14a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a14a-113">Requirements</span></span>



| <span data-ttu-id="5a14a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a14a-114">Requirement</span></span> | <span data-ttu-id="5a14a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5a14a-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a14a-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5a14a-116">Redistributable</span></span><br/> | <span data-ttu-id="5a14a-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a14a-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5a14a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5a14a-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="5a14a-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a14a-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a14a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a14a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a14a-121">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="5a14a-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5a14a-122">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="5a14a-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
