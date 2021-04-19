---
description: Il metodo Connect dell'oggetto merge connette un modulo a una funzionalità aggiuntiva. Il modulo deve essere già stato Unito nel database o verrà unito al database. La funzionalità deve esistere prima di chiamare questa funzione.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Metodo merge. Connect (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327322"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="9bebe-105">Merge. Connect (metodo)</span><span class="sxs-lookup"><span data-stu-id="9bebe-105">Merge.Connect method</span></span>

<span data-ttu-id="9bebe-106">Il metodo **Connect** dell'oggetto [**merge**](merge-object.md) connette un modulo a una funzionalità aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="9bebe-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="9bebe-107">Il modulo deve essere già stato Unito nel database o verrà unito al database.</span><span class="sxs-lookup"><span data-stu-id="9bebe-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="9bebe-108">La funzionalità deve esistere prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9bebe-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="9bebe-109">Le modifiche apportate al database non vengono salvate su disco a meno che non venga chiamato il metodo [**ChiudiDatabase**](merge-closedatabase.md) con *BCommit* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="9bebe-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bebe-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bebe-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="9bebe-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bebe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bebe-112">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="9bebe-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="9bebe-113">Nome di una funzionalità già esistente nel database.</span><span class="sxs-lookup"><span data-stu-id="9bebe-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bebe-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bebe-114">Return value</span></span>

<span data-ttu-id="9bebe-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9bebe-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bebe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bebe-116">Remarks</span></span>

<span data-ttu-id="9bebe-117">Gli errori possono essere recuperati tramite la proprietà [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="9bebe-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="9bebe-118">Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.</span><span class="sxs-lookup"><span data-stu-id="9bebe-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="9bebe-119">C++</span><span class="sxs-lookup"><span data-stu-id="9bebe-119">C++</span></span>

<span data-ttu-id="9bebe-120">Vedere funzione [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) .</span><span class="sxs-lookup"><span data-stu-id="9bebe-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bebe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bebe-121">Requirements</span></span>



| <span data-ttu-id="9bebe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bebe-122">Requirement</span></span> | <span data-ttu-id="9bebe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9bebe-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bebe-124">Versione</span><span class="sxs-lookup"><span data-stu-id="9bebe-124">Version</span></span><br/> | <span data-ttu-id="9bebe-125">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9bebe-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="9bebe-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bebe-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9bebe-127"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bebe-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="9bebe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9bebe-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bebe-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bebe-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
