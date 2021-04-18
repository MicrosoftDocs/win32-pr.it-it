---
title: Metodo External. download
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo di download avvia il download di un set di elementi multimediali.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Metodo di download Media Player Windows
- Metodo di download Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo di download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324566"
---
# <a name="externaldownload-method"></a><span data-ttu-id="f2615-108">Metodo External. download</span><span class="sxs-lookup"><span data-stu-id="f2615-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="f2615-109">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="f2615-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f2615-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f2615-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f2615-111">Il metodo di **download** avvia il download di un set di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="f2615-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2615-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2615-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="f2615-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2615-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2615-114">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f2615-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2615-115">[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo di elemento da scaricare.</span><span class="sxs-lookup"><span data-stu-id="f2615-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="f2615-116">Ad esempio, CPTrackID specifica che devono essere scaricate una o più tracce.</span><span class="sxs-lookup"><span data-stu-id="f2615-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="f2615-117">*ID* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f2615-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2615-118">**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi multimediali da scaricare.</span><span class="sxs-lookup"><span data-stu-id="f2615-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2615-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2615-119">Return value</span></span>

<span data-ttu-id="f2615-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f2615-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2615-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2615-121">Requirements</span></span>



| <span data-ttu-id="f2615-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2615-122">Requirement</span></span> | <span data-ttu-id="f2615-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f2615-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2615-124">Versione</span><span class="sxs-lookup"><span data-stu-id="f2615-124">Version</span></span><br/> | <span data-ttu-id="f2615-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f2615-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f2615-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f2615-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2615-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2615-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2615-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2615-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2615-129">**Download del contenuto multimediale**</span><span class="sxs-lookup"><span data-stu-id="f2615-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="f2615-130">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="f2615-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f2615-131">**External. Buy**</span><span class="sxs-lookup"><span data-stu-id="f2615-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="f2615-132">**IWMPContentPartner::D ownload**</span><span class="sxs-lookup"><span data-stu-id="f2615-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





