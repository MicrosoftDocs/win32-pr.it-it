---
description: Cancella tutti gli oggetti attributo dalla raccolta.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Metodo Attributes. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330376"
---
# <a name="attributesclear-method"></a><span data-ttu-id="6c778-103">Metodo Attributes. Clear</span><span class="sxs-lookup"><span data-stu-id="6c778-103">Attributes.Clear method</span></span>

<span data-ttu-id="6c778-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c778-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="6c778-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="6c778-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="6c778-106">Il metodo **Clear** Cancella tutti gli oggetti [**attribute**](attribute.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6c778-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c778-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c778-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="6c778-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c778-108">Parameters</span></span>

<span data-ttu-id="6c778-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6c778-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c778-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c778-110">Return value</span></span>

<span data-ttu-id="6c778-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6c778-111">This method does not return a value.</span></span> <span data-ttu-id="6c778-112">Un'applicazione che usa questo metodo deve contenere codice per gestire un'eccezione generata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6c778-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c778-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c778-113">Requirements</span></span>



| <span data-ttu-id="6c778-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c778-114">Requirement</span></span> | <span data-ttu-id="6c778-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6c778-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c778-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6c778-116">End of client support</span></span><br/> | <span data-ttu-id="6c778-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c778-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6c778-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6c778-118">End of server support</span></span><br/> | <span data-ttu-id="6c778-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c778-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6c778-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6c778-120">Redistributable</span></span><br/>       | <span data-ttu-id="6c778-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c778-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c778-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6c778-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6c778-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c778-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c778-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c778-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c778-125">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="6c778-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="6c778-126">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="6c778-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
