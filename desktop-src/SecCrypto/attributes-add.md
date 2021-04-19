---
description: Aggiunge un oggetto attributo alla raccolta.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Metodo Attributes. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332692"
---
# <a name="attributesadd-method"></a><span data-ttu-id="7e285-103">Metodo Attributes. Add</span><span class="sxs-lookup"><span data-stu-id="7e285-103">Attributes.Add method</span></span>

<span data-ttu-id="7e285-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e285-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7e285-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="7e285-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="7e285-106">Il metodo **Add** aggiunge un oggetto [**attribute**](attribute.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="7e285-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e285-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e285-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="7e285-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e285-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e285-109">*Attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e285-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e285-110">Oggetto [**attributo**](attribute.md) da aggiungere alla fine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7e285-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e285-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e285-111">Return value</span></span>

<span data-ttu-id="7e285-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7e285-112">This method does not return a value.</span></span> <span data-ttu-id="7e285-113">Un'applicazione che usa questo metodo deve contenere codice per gestire un'eccezione generata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7e285-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e285-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e285-114">Requirements</span></span>



| <span data-ttu-id="7e285-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e285-115">Requirement</span></span> | <span data-ttu-id="7e285-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7e285-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e285-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7e285-117">End of client support</span></span><br/> | <span data-ttu-id="7e285-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e285-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7e285-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7e285-119">End of server support</span></span><br/> | <span data-ttu-id="7e285-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e285-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e285-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7e285-121">Redistributable</span></span><br/>       | <span data-ttu-id="7e285-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e285-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7e285-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7e285-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7e285-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e285-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e285-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e285-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e285-126">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="7e285-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7e285-127">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="7e285-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
