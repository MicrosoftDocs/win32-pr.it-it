---
title: Cdromcollection. Count
description: La proprietà Count recupera il numero di unità CD e DVD disponibili nel sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Windows Media Player cdromcollection. Count
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333136"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="ad78d-104">Cdromcollection. Count</span><span class="sxs-lookup"><span data-stu-id="ad78d-104">CdromCollection.count</span></span>

<span data-ttu-id="ad78d-105">La proprietà **count** Recupera il numero di unità CD e DVD disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ad78d-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="ad78d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ad78d-106">Possible Values</span></span>

<span data-ttu-id="ad78d-107">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ad78d-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad78d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad78d-108">Remarks</span></span>

<span data-ttu-id="ad78d-109">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ad78d-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ad78d-110">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ad78d-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ad78d-111">Le unità DVD-ROM vengono conteggiate esattamente come le unità CD.</span><span class="sxs-lookup"><span data-stu-id="ad78d-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="ad78d-112">Tuttavia, il controllo Media Player Windows supporta solo la funzionalità DVD per Windows XP o sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="ad78d-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="ad78d-113">In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="ad78d-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="ad78d-114">**Windows Media Player 10 Mobile:** Questo metodo restituisce sempre 0.</span><span class="sxs-lookup"><span data-stu-id="ad78d-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="ad78d-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad78d-115">Examples</span></span>

<span data-ttu-id="ad78d-116">Nell'esempio JScript seguente viene usato *cdromcollection*. **conteggio** per visualizzare il numero di unità CD e DVD disponibili nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ad78d-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="ad78d-117">L'oggetto Player è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ad78d-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="ad78d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad78d-118">Requirements</span></span>



| <span data-ttu-id="ad78d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad78d-119">Requirement</span></span> | <span data-ttu-id="ad78d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ad78d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad78d-121">Versione</span><span class="sxs-lookup"><span data-stu-id="ad78d-121">Version</span></span><br/> | <span data-ttu-id="ad78d-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="ad78d-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="ad78d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ad78d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad78d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad78d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad78d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad78d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad78d-126">**Oggetto cdromcollection**</span><span class="sxs-lookup"><span data-stu-id="ad78d-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ad78d-127">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ad78d-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ad78d-128">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ad78d-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





