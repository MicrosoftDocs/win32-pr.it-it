---
description: Rimuove l'oggetto OID specificato dalla raccolta.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Metodo OID. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325155"
---
# <a name="oidsremove-method"></a><span data-ttu-id="fbbd2-103">Metodo OID. Remove</span><span class="sxs-lookup"><span data-stu-id="fbbd2-103">OIDs.Remove method</span></span>

<span data-ttu-id="fbbd2-104">\[Il metodo **Remove** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fbbd2-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbbd2-105">Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fbbd2-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fbbd2-106">Il metodo **Remove** rimuove l'oggetto [**OID**](oid.md) specificato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="fbbd2-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbd2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbbd2-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="fbbd2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbbd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbbd2-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fbbd2-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbbd2-110">Indice dell'oggetto [**OID**](oid.md) da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fbbd2-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="fbbd2-111">Può essere un indice nella raccolta o il valore punteggiato dell'OID.</span><span class="sxs-lookup"><span data-stu-id="fbbd2-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbbd2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbbd2-112">Return value</span></span>

<span data-ttu-id="fbbd2-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fbbd2-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbbd2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbbd2-114">Requirements</span></span>



| <span data-ttu-id="fbbd2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbd2-115">Requirement</span></span> | <span data-ttu-id="fbbd2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fbbd2-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbd2-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fbbd2-117">Redistributable</span></span><br/> | <span data-ttu-id="fbbd2-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbbd2-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fbbd2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbd2-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="fbbd2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbd2-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
