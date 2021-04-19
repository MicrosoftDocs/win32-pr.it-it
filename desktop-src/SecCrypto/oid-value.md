---
description: Imposta o Recupera il valore del numero punteggiato dell'OID dell'identificatore.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Proprietà Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333564"
---
# <a name="oidvalue-property"></a><span data-ttu-id="2b46c-103">OID. Proprietà Value</span><span class="sxs-lookup"><span data-stu-id="2b46c-103">OID.Value property</span></span>

<span data-ttu-id="2b46c-104">\[La proprietà **value** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2b46c-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b46c-105">Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2b46c-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2b46c-106">La proprietà **value** imposta o Recupera il valore del numero punteggiato dell'OID dell'identificatore.</span><span class="sxs-lookup"><span data-stu-id="2b46c-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b46c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b46c-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="2b46c-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2b46c-108">Property value</span></span>

<span data-ttu-id="2b46c-109">Valore del numero punteggiato dell'OID dell'identificatore.</span><span class="sxs-lookup"><span data-stu-id="2b46c-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="2b46c-110">Per i valori possibili, vedere Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="2b46c-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b46c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b46c-111">Remarks</span></span>

<span data-ttu-id="2b46c-112">Se la proprietà **value** è impostata, la proprietà [**FriendlyName**](oid-friendlyname.md) viene impostata sul nome visualizzato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2b46c-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="2b46c-113">Se la proprietà **FriendlyName** è impostata, la proprietà **value** viene impostata sul valore punteggiato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2b46c-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b46c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b46c-114">Requirements</span></span>



| <span data-ttu-id="2b46c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b46c-115">Requirement</span></span> | <span data-ttu-id="2b46c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2b46c-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b46c-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2b46c-117">Redistributable</span></span><br/> | <span data-ttu-id="2b46c-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b46c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2b46c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2b46c-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="2b46c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b46c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b46c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b46c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b46c-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="2b46c-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
