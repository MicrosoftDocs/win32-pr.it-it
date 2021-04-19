---
description: Aggiunge l'oggetto OID specificato alla raccolta.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OID. Add, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329613"
---
# <a name="oidsadd-method"></a><span data-ttu-id="d9922-103">OID. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="d9922-103">OIDs.Add method</span></span>

<span data-ttu-id="d9922-104">\[Il metodo **Add** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d9922-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d9922-105">Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d9922-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d9922-106">Il metodo **Add** aggiunge l'oggetto [**OID**](oid.md) specificato alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9922-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9922-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9922-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="d9922-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9922-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9922-109">*OID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9922-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9922-110">Oggetto [**OID**](oid.md) da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9922-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="d9922-111">L'oggetto **OID** viene aggiunto nell'ordinamento in base al relativo valore punteggiato.</span><span class="sxs-lookup"><span data-stu-id="d9922-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9922-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9922-112">Return value</span></span>

<span data-ttu-id="d9922-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d9922-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9922-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9922-114">Requirements</span></span>



| <span data-ttu-id="d9922-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9922-115">Requirement</span></span> | <span data-ttu-id="d9922-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d9922-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9922-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d9922-117">Redistributable</span></span><br/> | <span data-ttu-id="d9922-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d9922-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d9922-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d9922-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="d9922-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9922-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
