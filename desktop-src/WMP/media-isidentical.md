---
title: Metodo media. IsValid
description: Il metodo IsValid recupera un valore che indica se l'oggetto fornito è uguale a quello corrente. | Metodo media. IsValid
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Metodo di Media Player di Windows identico
- Metodo di Windows Media Player, classe multimediale
- Media class Media Player Windows, metodo identico
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329308"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="026fd-107">Metodo media. IsValid</span><span class="sxs-lookup"><span data-stu-id="026fd-107">Media.isIdentical method</span></span>

<span data-ttu-id="026fd-108">Il **Metodo IsValid** recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="026fd-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="026fd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="026fd-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="026fd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="026fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="026fd-111">*supporto* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="026fd-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026fd-112">Oggetto **multimediale** da confrontare con l'oggetto **multimediale** corrente.</span><span class="sxs-lookup"><span data-stu-id="026fd-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="026fd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="026fd-113">Return value</span></span>

<span data-ttu-id="026fd-114">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="026fd-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="026fd-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="026fd-115">Examples</span></span>

<span data-ttu-id="026fd-116">Nell'esempio JScript seguente viene usato il *supporto*. è **identico** per verificare se un elemento multimediale denominato newMedia è uguale all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="026fd-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="026fd-117">Se non sono uguali, viene riprodotto il nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="026fd-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="026fd-118">In caso contrario, i supporti correnti continueranno a essere riprodotti senza interruzioni.</span><span class="sxs-lookup"><span data-stu-id="026fd-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="026fd-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="026fd-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="026fd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="026fd-120">Requirements</span></span>



| <span data-ttu-id="026fd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="026fd-121">Requirement</span></span> | <span data-ttu-id="026fd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="026fd-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="026fd-123">Versione</span><span class="sxs-lookup"><span data-stu-id="026fd-123">Version</span></span><br/> | <span data-ttu-id="026fd-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="026fd-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="026fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="026fd-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="026fd-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="026fd-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="026fd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="026fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026fd-128">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="026fd-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





