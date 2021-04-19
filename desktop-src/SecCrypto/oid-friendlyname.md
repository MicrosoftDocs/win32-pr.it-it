---
description: Imposta o Recupera il nome visualizzato per l'identificatore.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. Proprietà FriendlyName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332009"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="2aafd-103">OID. Proprietà FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2aafd-103">OID.FriendlyName property</span></span>

<span data-ttu-id="2aafd-104">\[La proprietà **FriendlyName** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2aafd-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2aafd-105">Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2aafd-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2aafd-106">La proprietà **FriendlyName** imposta o Recupera il nome visualizzato per l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="2aafd-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aafd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aafd-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="2aafd-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2aafd-108">Property value</span></span>

<span data-ttu-id="2aafd-109">Nome visualizzato per l' [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="2aafd-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2aafd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2aafd-110">Remarks</span></span>

<span data-ttu-id="2aafd-111">Se la proprietà **FriendlyName** è impostata, la proprietà [**value**](oid-value.md) viene impostata sul valore punteggiato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2aafd-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="2aafd-112">Se la proprietà **value** è impostata, la proprietà **FriendlyName** viene impostata sul nome visualizzato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2aafd-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aafd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2aafd-113">Requirements</span></span>



| <span data-ttu-id="2aafd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aafd-114">Requirement</span></span> | <span data-ttu-id="2aafd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2aafd-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aafd-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2aafd-116">Redistributable</span></span><br/> | <span data-ttu-id="2aafd-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2aafd-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2aafd-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2aafd-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="2aafd-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aafd-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aafd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2aafd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aafd-121">**OID**</span><span class="sxs-lookup"><span data-stu-id="2aafd-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
