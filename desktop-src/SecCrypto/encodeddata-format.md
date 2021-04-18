---
description: Restituisce una rappresentazione di stringa dei dati codificati.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Metodo EncodedData. Format
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331604"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="849b0-103">Metodo EncodedData. Format</span><span class="sxs-lookup"><span data-stu-id="849b0-103">EncodedData.Format method</span></span>

<span data-ttu-id="849b0-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="849b0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="849b0-105">Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="849b0-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="849b0-106">Il metodo **Format** restituisce una rappresentazione di stringa dei dati codificati.</span><span class="sxs-lookup"><span data-stu-id="849b0-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="849b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="849b0-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="849b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="849b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849b0-109">*bMultiLines* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="849b0-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="849b0-110">Valore booleano che indica se la stringa restituita contiene più righe.</span><span class="sxs-lookup"><span data-stu-id="849b0-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="849b0-111">Se **true**, la stringa restituita può contenere più righe separate da **vbCrLf**.</span><span class="sxs-lookup"><span data-stu-id="849b0-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="849b0-112">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="849b0-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849b0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="849b0-113">Return value</span></span>

<span data-ttu-id="849b0-114">Stringa leggibile che rappresenta i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="849b0-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="849b0-115">Se capicol non comprende i dati codificati, viene restituita una rappresentazione esadecimale dei dati.</span><span class="sxs-lookup"><span data-stu-id="849b0-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="849b0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="849b0-116">Remarks</span></span>

<span data-ttu-id="849b0-117">Il formato della stringa restituita può variare tra diverse versioni di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="849b0-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="849b0-118">Non fare affidamento su un particolare formato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="849b0-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="849b0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="849b0-119">Requirements</span></span>



| <span data-ttu-id="849b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="849b0-120">Requirement</span></span> | <span data-ttu-id="849b0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="849b0-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="849b0-122">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="849b0-122">End of client support</span></span><br/> | <span data-ttu-id="849b0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="849b0-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="849b0-124">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="849b0-124">End of server support</span></span><br/> | <span data-ttu-id="849b0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="849b0-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="849b0-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="849b0-126">Redistributable</span></span><br/>       | <span data-ttu-id="849b0-127">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="849b0-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="849b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="849b0-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="849b0-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="849b0-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849b0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="849b0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849b0-131">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="849b0-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
