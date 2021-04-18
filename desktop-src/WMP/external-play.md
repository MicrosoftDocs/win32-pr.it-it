---
title: Metodo External. Play
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Play indica a Windows Media Player di riprodurre un set di elementi multimediali.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Metodo di riproduzione Media Player Windows
- Metodo Play Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo Play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324550"
---
# <a name="externalplay-method"></a><span data-ttu-id="60e3b-108">Metodo External. Play</span><span class="sxs-lookup"><span data-stu-id="60e3b-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="60e3b-109">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="60e3b-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="60e3b-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="60e3b-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="60e3b-111">Il metodo **Play** indica a Windows Media Player di riprodurre un set di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="60e3b-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e3b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60e3b-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="60e3b-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="60e3b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e3b-114">*LibraryLocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60e3b-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e3b-115">[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo degli elementi multimediali da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="60e3b-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="60e3b-116">Ad esempio, CPAlbumID specifica che uno o più album devono essere riprodotti.</span><span class="sxs-lookup"><span data-stu-id="60e3b-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="60e3b-117">*LibraryLocationIDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60e3b-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60e3b-118">**Stringa** contenente gli identificatori, delimitati da punti e virgola, degli elementi multimediali da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="60e3b-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e3b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60e3b-119">Return value</span></span>

<span data-ttu-id="60e3b-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="60e3b-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e3b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60e3b-121">Requirements</span></span>



| <span data-ttu-id="60e3b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60e3b-122">Requirement</span></span> | <span data-ttu-id="60e3b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="60e3b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60e3b-124">Versione</span><span class="sxs-lookup"><span data-stu-id="60e3b-124">Version</span></span><br/> | <span data-ttu-id="60e3b-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="60e3b-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="60e3b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="60e3b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="60e3b-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60e3b-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e3b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60e3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e3b-129">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="60e3b-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





