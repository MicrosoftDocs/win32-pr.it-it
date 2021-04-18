---
title: Cdrom. driveSpecifier
description: La proprietà driveSpecifier recupera la lettera dell'unità CD o DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Media Player Windows cdrom. driveSpecifier
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517523"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="5eefb-104">Cdrom. driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="5eefb-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="5eefb-105">La proprietà **driveSpecifier** recupera la lettera dell'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="5eefb-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="5eefb-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5eefb-106">Possible Values</span></span>

<span data-ttu-id="5eefb-107">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5eefb-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eefb-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eefb-108">Remarks</span></span>

<span data-ttu-id="5eefb-109">In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="5eefb-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="5eefb-110">Questa proprietà recupera un identificatore di unità per un indice di unità in base zero nell'intervallo recuperato utilizzando *cdromcollection*. **conteggio**.</span><span class="sxs-lookup"><span data-stu-id="5eefb-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="5eefb-111">Il valore recuperato assume il formato *x*:, dove *x* rappresenta la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="5eefb-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="5eefb-112">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="5eefb-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5eefb-113">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5eefb-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5eefb-114">**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="5eefb-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5eefb-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5eefb-115">Examples</span></span>

<span data-ttu-id="5eefb-116">Nell'esempio JScript seguente viene usato *CDROM*. **driveSpecifier** per riempire un'area di testo HTML denominata testo con un elenco delimitato da virgole di unità CD e DVD disponibili.</span><span class="sxs-lookup"><span data-stu-id="5eefb-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="5eefb-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5eefb-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="5eefb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eefb-118">Requirements</span></span>



| <span data-ttu-id="5eefb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eefb-119">Requirement</span></span> | <span data-ttu-id="5eefb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5eefb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5eefb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eefb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5eefb-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5eefb-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5eefb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eefb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5eefb-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5eefb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5eefb-125">Versione</span><span class="sxs-lookup"><span data-stu-id="5eefb-125">Version</span></span><br/>                  | <span data-ttu-id="5eefb-126">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5eefb-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="5eefb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5eefb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eefb-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eefb-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eefb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eefb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eefb-130">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="5eefb-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="5eefb-131">**Cdromcollection. Count**</span><span class="sxs-lookup"><span data-stu-id="5eefb-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="5eefb-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5eefb-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5eefb-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5eefb-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





