---
title: Metodo IWMPCdromCollection getByDriveSpecifier
description: Il metodo getByDriveSpecifier restituisce un'interfaccia IWMPCdrom associata a una lettera di unità specifica.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- Metodo getByDriveSpecifier Windows Media Player
- Metodo getByDriveSpecifier Windows Media Player, interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection Windows Media Player, metodo getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329292"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="c3f8a-106">Metodo IWMPCdromCollection:: getByDriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="c3f8a-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="c3f8a-107">Il metodo **getByDriveSpecifier** restituisce un'interfaccia **IWMPCdrom** associata a una lettera di unità specifica.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f8a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3f8a-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="c3f8a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3f8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f8a-110">*bstrDriveSpecifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f8a-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f8a-111">**System. String** che corrisponde alla lettera di unità seguita da un carattere due punti (":").</span><span class="sxs-lookup"><span data-stu-id="c3f8a-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f8a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3f8a-112">Return value</span></span>

<span data-ttu-id="c3f8a-113">Interfaccia **wmplib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="c3f8a-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f8a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3f8a-114">Remarks</span></span>

<span data-ttu-id="c3f8a-115">Le lettere di unità devono essere specificate nel formato *x*:, dove *x* rappresenta la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="c3f8a-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c3f8a-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c3f8a-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c3f8a-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="c3f8a-118">Examples</span></span>

<span data-ttu-id="c3f8a-119">Nell'esempio seguente viene usato **getByDriveSpecifier** per ottenere l'interfaccia **IWMPCdrom** che corrisponde a una lettera di unità fornita dall'utente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="c3f8a-120">Viene quindi chiamato il metodo **IWMPCdrom. EJECT** per rimuovere l'unità specificata.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="c3f8a-121">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c3f8a-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="c3f8a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3f8a-122">Requirements</span></span>



| <span data-ttu-id="c3f8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f8a-123">Requirement</span></span> | <span data-ttu-id="c3f8a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f8a-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f8a-125">Versione</span><span class="sxs-lookup"><span data-stu-id="c3f8a-125">Version</span></span><br/>   | <span data-ttu-id="c3f8a-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c3f8a-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c3f8a-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3f8a-127">Namespace</span></span><br/> | <span data-ttu-id="c3f8a-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c3f8a-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3f8a-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3f8a-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f8a-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f8a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3f8a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f8a-132">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3f8a-133">**IWMPCdrom. EJECT (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3f8a-134">**Interfaccia IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3f8a-135">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3f8a-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f8a-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





