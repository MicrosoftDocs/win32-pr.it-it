---
description: Rimuove dall'insieme un oggetto attributo indicizzato.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Metodo Attributes. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330273"
---
# <a name="attributesremove-method"></a><span data-ttu-id="5f161-103">Metodo Attributes. Remove</span><span class="sxs-lookup"><span data-stu-id="5f161-103">Attributes.Remove method</span></span>

<span data-ttu-id="5f161-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f161-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="5f161-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5f161-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5f161-106">Il metodo **Remove** rimuove un oggetto [**attributo**](attribute.md) indicizzato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5f161-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f161-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f161-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="5f161-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f161-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f161-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5f161-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f161-110">Indice dell'oggetto [**attributo**](attribute.md) da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5f161-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f161-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f161-111">Return value</span></span>

<span data-ttu-id="5f161-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5f161-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f161-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f161-113">Remarks</span></span>

<span data-ttu-id="5f161-114">Le applicazioni che usano questo metodo devono contenere codice per gestire un'eccezione generata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5f161-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f161-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f161-115">Requirements</span></span>



| <span data-ttu-id="5f161-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f161-116">Requirement</span></span> | <span data-ttu-id="5f161-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f161-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f161-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5f161-118">End of client support</span></span><br/> | <span data-ttu-id="5f161-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f161-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5f161-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5f161-120">End of server support</span></span><br/> | <span data-ttu-id="5f161-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f161-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5f161-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5f161-122">Redistributable</span></span><br/>       | <span data-ttu-id="5f161-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f161-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5f161-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5f161-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5f161-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f161-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f161-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f161-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f161-127">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="5f161-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5f161-128">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="5f161-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
