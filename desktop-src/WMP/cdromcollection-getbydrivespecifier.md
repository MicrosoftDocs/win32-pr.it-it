---
title: Cdromcollection. getByDriveSpecifier, metodo
description: Il metodo getByDriveSpecifier recupera l'oggetto cdrom associato a una lettera di unità specifica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Metodo getByDriveSpecifier Windows Media Player
- Metodo getByDriveSpecifier Windows Media Player, classe cdromcollection
- Classe cdromcollection Windows Media Player, metodo getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333135"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="3a330-106">Cdromcollection. getByDriveSpecifier, metodo</span><span class="sxs-lookup"><span data-stu-id="3a330-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="3a330-107">Il metodo **getByDriveSpecifier** recupera l'oggetto **CDROM** associato a una lettera di unità specifica.</span><span class="sxs-lookup"><span data-stu-id="3a330-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a330-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a330-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="3a330-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a330-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a330-110">*driveSpecifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a330-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a330-111">**Stringa** contenente la lettera di unità seguita da un carattere due punti (":").</span><span class="sxs-lookup"><span data-stu-id="3a330-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a330-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a330-112">Return value</span></span>

<span data-ttu-id="3a330-113">Questo metodo restituisce un oggetto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="3a330-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a330-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a330-114">Remarks</span></span>

<span data-ttu-id="3a330-115">Le lettere di unità devono essere specificate nel formato *x*:, dove *x* rappresenta la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="3a330-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="3a330-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3a330-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3a330-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3a330-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3a330-118">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3a330-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="3a330-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a330-119">Examples</span></span>

<span data-ttu-id="3a330-120">Nell'esempio JScript seguente viene usato *cdromcollection*. **getByDriveSpecifier** per recuperare l'oggetto **CDROM** che corrisponde a una lettera di unità fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3a330-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="3a330-121">È stato creato un elemento di testo HTML, con nome = "testo", per l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3a330-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="3a330-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3a330-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="3a330-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a330-123">Requirements</span></span>



| <span data-ttu-id="3a330-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a330-124">Requirement</span></span> | <span data-ttu-id="3a330-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3a330-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a330-126">Versione</span><span class="sxs-lookup"><span data-stu-id="3a330-126">Version</span></span><br/> | <span data-ttu-id="3a330-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3a330-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3a330-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a330-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a330-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a330-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a330-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a330-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a330-131">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="3a330-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="3a330-132">**Cdrom. EJECT**</span><span class="sxs-lookup"><span data-stu-id="3a330-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="3a330-133">**Oggetto cdromcollection**</span><span class="sxs-lookup"><span data-stu-id="3a330-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="3a330-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a330-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3a330-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a330-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





