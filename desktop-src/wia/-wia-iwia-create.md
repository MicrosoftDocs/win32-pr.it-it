---
description: Il metodo Create dell'oggetto Wia crea una connessione al dispositivo WIA (Windows Image Acquisition) specificato e restituisce un oggetto Item che rappresenta il dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Metodo Wia.Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841332"
---
# <a name="wiacreate-method"></a><span data-ttu-id="49173-103">Metodo Wia.Create</span><span class="sxs-lookup"><span data-stu-id="49173-103">Wia.Create method</span></span>

<span data-ttu-id="49173-104">Il **metodo Create** dell'oggetto [**Wia**](-wia-wia.md) crea una connessione al dispositivo WIA (Windows Image Acquisition) specificato e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49173-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="49173-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49173-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="49173-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49173-107">*Dispositivo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="49173-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49173-108">Tipo: **\* VARIANT**</span><span class="sxs-lookup"><span data-stu-id="49173-108">Type: **VARIANT\***</span></span>

<span data-ttu-id="49173-109">Specifica il dispositivo WIA a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="49173-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49173-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49173-110">Return value</span></span>

<span data-ttu-id="49173-111">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="49173-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="49173-112">Se ha esito positivo, questo metodo restituisce un [**oggetto Item**](-wia-item.md) che rappresenta un dispositivo hardware WIA (un elemento radice).</span><span class="sxs-lookup"><span data-stu-id="49173-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="49173-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="49173-113">Remarks</span></span>

<span data-ttu-id="49173-114">Il *parametro Device* specifica un oggetto [**DeviceInfo**](-wia-deviceinfo.md) passando l'oggetto stesso, il relativo indice da un oggetto raccolta o il valore della relativa [**proprietà Id.**](-wia-iwiadeviceinfo-id.md)</span><span class="sxs-lookup"><span data-stu-id="49173-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="49173-115">Passare **Nothing** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49173-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="49173-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="49173-116">Examples</span></span>

<span data-ttu-id="49173-117">Gli esempi DI VBScript seguenti illustrano l'uso del **metodo Create.**</span><span class="sxs-lookup"><span data-stu-id="49173-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="49173-118">Il primo esempio passa [**un oggetto DeviceInfo**](-wia-deviceinfo.md) al **metodo Create.**</span><span class="sxs-lookup"><span data-stu-id="49173-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="49173-119">Si noti che il passaggio della proprietà [**Id**](-wia-iwiadeviceinfo-id.md) dell'oggetto determina esattamente lo stesso comportamento.</span><span class="sxs-lookup"><span data-stu-id="49173-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="49173-120">Nell'esempio successivo l'applicazione chiamante passa l'indice [**dell'oggetto DeviceInfo**](-wia-deviceinfo.md) nella raccolta al **metodo Create.**</span><span class="sxs-lookup"><span data-stu-id="49173-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="49173-121">L'esempio successivo passa **Nothing** al **metodo Create** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49173-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="49173-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49173-122">Requirements</span></span>



| <span data-ttu-id="49173-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49173-123">Requirement</span></span> | <span data-ttu-id="49173-124">Valore</span><span class="sxs-lookup"><span data-stu-id="49173-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49173-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49173-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49173-126">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="49173-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49173-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49173-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49173-128">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49173-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="49173-129">DLL</span><span class="sxs-lookup"><span data-stu-id="49173-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49173-130"><dt>Wiascr.dll (versione 4.90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="49173-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




