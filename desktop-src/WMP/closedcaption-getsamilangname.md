---
title: ClosedCaption. getSAMILangName, metodo
description: Il metodo getSAMILangName Recupera il nome di una lingua supportata dal file SAMI corrente.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Metodo getSAMILangName Windows Media Player
- Metodo getSAMILangName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, metodo getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329086"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="8e449-106">ClosedCaption. getSAMILangName, metodo</span><span class="sxs-lookup"><span data-stu-id="8e449-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="8e449-107">Il metodo **getSAMILangName** Recupera il nome di una lingua supportata dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="8e449-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e449-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e449-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="8e449-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e449-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e449-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8e449-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e449-111">**Numero** (**Long**) che specifica l'indice del nome del linguaggio da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8e449-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e449-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e449-112">Return value</span></span>

<span data-ttu-id="8e449-113">Questo metodo restituisce una **stringa** contenente il nome del linguaggio come specificato nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="8e449-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e449-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e449-114">Remarks</span></span>

<span data-ttu-id="8e449-115">Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="8e449-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="8e449-116">Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="8e449-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="8e449-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8e449-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e449-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e449-118">Requirements</span></span>



| <span data-ttu-id="8e449-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e449-119">Requirement</span></span> | <span data-ttu-id="8e449-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8e449-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e449-121">Versione</span><span class="sxs-lookup"><span data-stu-id="8e449-121">Version</span></span><br/> | <span data-ttu-id="8e449-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8e449-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="8e449-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8e449-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e449-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e449-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e449-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e449-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e449-126">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="8e449-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8e449-127">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="8e449-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="8e449-128">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="8e449-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





