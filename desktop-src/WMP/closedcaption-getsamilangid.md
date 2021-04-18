---
title: ClosedCaption. getSAMILangID, metodo
description: Il metodo getSAMILangID recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Metodo getSAMILangID Windows Media Player
- Metodo getSAMILangID Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, metodo getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333932"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="6e083-106">ClosedCaption. getSAMILangID, metodo</span><span class="sxs-lookup"><span data-stu-id="6e083-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="6e083-107">Il metodo **getSAMILangID** recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="6e083-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e083-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e083-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="6e083-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e083-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e083-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6e083-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e083-111">**Numero** (**Long**) che specifica l'indice dell'LCID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6e083-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e083-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e083-112">Return value</span></span>

<span data-ttu-id="6e083-113">Questo metodo restituisce un **numero** (**Long**) contenente l'identificatore LCID della lingua con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6e083-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e083-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e083-114">Remarks</span></span>

<span data-ttu-id="6e083-115">Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="6e083-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="6e083-116">Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="6e083-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="6e083-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6e083-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e083-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e083-118">Requirements</span></span>



| <span data-ttu-id="6e083-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e083-119">Requirement</span></span> | <span data-ttu-id="6e083-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6e083-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e083-121">Versione</span><span class="sxs-lookup"><span data-stu-id="6e083-121">Version</span></span><br/> | <span data-ttu-id="6e083-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6e083-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6e083-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6e083-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e083-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e083-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e083-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e083-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e083-126">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="6e083-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6e083-127">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="6e083-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





