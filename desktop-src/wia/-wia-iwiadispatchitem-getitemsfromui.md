---
description: Il metodo GetItemsFromUI dell'oggetto Item Visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130019"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="6a648-103">Item. GetItemsFromUI, metodo</span><span class="sxs-lookup"><span data-stu-id="6a648-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="6a648-104">Il metodo **GetItemsFromUI** dell'oggetto [**Item**](-wia-item.md) Visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a648-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a648-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a648-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="6a648-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a648-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a648-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a648-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a648-108">Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="6a648-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="6a648-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="6a648-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6a648-110">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a648-110">Default.</span></span> <span data-ttu-id="6a648-111">\[in \] specifica il comportamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6a648-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="6a648-112">I valori validi per questo parametro sono identici a quelli per il parametro *è* del metodo [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .</span><span class="sxs-lookup"><span data-stu-id="6a648-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a648-113">*Finalità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a648-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a648-114">Tipo: **WiaIntent**</span><span class="sxs-lookup"><span data-stu-id="6a648-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="6a648-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="6a648-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6a648-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a648-116">Default.</span></span> <span data-ttu-id="6a648-117">\[in \] specifica il tipo di dati che l'immagine deve rappresentare.</span><span class="sxs-lookup"><span data-stu-id="6a648-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="6a648-118">Per un elenco di valori per finalità immagine, vedere [**costanti per finalità di immagine**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="6a648-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a648-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a648-119">Return value</span></span>

<span data-ttu-id="6a648-120">Tipo: **ICollection**</span><span class="sxs-lookup"><span data-stu-id="6a648-120">Type: **ICollection**</span></span>

<span data-ttu-id="6a648-121">Questo metodo restituisce una raccolta di oggetti [**Item**](-wia-item.md) che rappresentano gli elementi selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6a648-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="6a648-122">Se non è selezionato alcun elemento, l'insieme è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6a648-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a648-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a648-123">Remarks</span></span>

<span data-ttu-id="6a648-124">Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library".</span><span class="sxs-lookup"><span data-stu-id="6a648-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="6a648-125">Questo metodo si applica solo ai dispositivi (elementi radice).</span><span class="sxs-lookup"><span data-stu-id="6a648-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="6a648-126">Il metodo restituisce una raccolta di oggetti [**Item**](-wia-item.md) che rappresentano le immagini o i clip audio selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6a648-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="6a648-127">Se l'utente non seleziona elementi, il metodo restituisce una raccolta vuota.</span><span class="sxs-lookup"><span data-stu-id="6a648-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="6a648-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a648-128">Examples</span></span>

<span data-ttu-id="6a648-129">Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetItemsFromUI** per consentire a un utente di selezionare immagini da una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6a648-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="6a648-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a648-130">Requirements</span></span>



| <span data-ttu-id="6a648-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a648-131">Requirement</span></span> | <span data-ttu-id="6a648-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6a648-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a648-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a648-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6a648-134">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6a648-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a648-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a648-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6a648-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a648-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a648-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6a648-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a648-138"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6a648-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




