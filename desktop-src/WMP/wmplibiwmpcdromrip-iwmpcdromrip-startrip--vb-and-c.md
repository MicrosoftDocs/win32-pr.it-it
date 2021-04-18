---
title: Metodo IWMPCdromRip startRip
description: Il metodo startRip strappa il CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- Metodo startRip Windows Media Player
- Metodo startRip Windows Media Player, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip Windows Media Player, metodo startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329286"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="0ac3c-106">Metodo IWMPCdromRip:: startRip</span><span class="sxs-lookup"><span data-stu-id="0ac3c-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="0ac3c-107">Il metodo **startRip** strappa il CD.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac3c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac3c-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="0ac3c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ac3c-109">Parameters</span></span>

<span data-ttu-id="0ac3c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ac3c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ac3c-111">Return value</span></span>

<span data-ttu-id="0ac3c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac3c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ac3c-113">Remarks</span></span>

<span data-ttu-id="0ac3c-114">La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="0ac3c-115">Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="0ac3c-116">Per ulteriori informazioni sulle preferenze utente per il ritaglio di CD, vedere la sezione relativa alla copia di musica da CDs nella Guida di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac3c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ac3c-117">Requirements</span></span>



| <span data-ttu-id="0ac3c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac3c-118">Requirement</span></span> | <span data-ttu-id="0ac3c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0ac3c-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac3c-120">Versione</span><span class="sxs-lookup"><span data-stu-id="0ac3c-120">Version</span></span><br/>   | <span data-ttu-id="0ac3c-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0ac3c-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0ac3c-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ac3c-122">Namespace</span></span><br/> | <span data-ttu-id="0ac3c-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ac3c-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ac3c-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ac3c-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ac3c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac3c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac3c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ac3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac3c-127">**Interfaccia IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0ac3c-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ac3c-128">**IWMPCdromRip.stopRip**</span><span class="sxs-lookup"><span data-stu-id="0ac3c-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ac3c-129">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="0ac3c-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





