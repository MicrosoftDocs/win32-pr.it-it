---
description: Il metodo di trasferimento dell'oggetto Item trasferisce i dati da un dispositivo a un file. Questo metodo si applica solo agli elementi del tipo di dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308225"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="ff419-104">Item. Transfer (metodo)</span><span class="sxs-lookup"><span data-stu-id="ff419-104">Item.Transfer method</span></span>

<span data-ttu-id="ff419-105">Il metodo di **trasferimento** dell'oggetto [**Item**](-wia-item.md) trasferisce i dati da un dispositivo a un file.</span><span class="sxs-lookup"><span data-stu-id="ff419-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="ff419-106">Questo metodo si applica solo agli elementi del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff419-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff419-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff419-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="ff419-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff419-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff419-109">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff419-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff419-110">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff419-110">Type: **BSTR**</span></span>

<span data-ttu-id="ff419-111">Specifica il nome del file in cui vengono trasferiti i dati.</span><span class="sxs-lookup"><span data-stu-id="ff419-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="ff419-112">*AsyncTransfer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff419-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff419-113">Tipo: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ff419-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="ff419-114">Valore booleano che specifica se il trasferimento deve essere eseguito come chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ff419-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="ff419-115">(Variante \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ff419-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="ff419-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff419-116">Default.</span></span> <span data-ttu-id="ff419-117">Impostare questo valore su **true** se la chiamata deve essere asincrona (vedere la **sezione Osservazioni**).</span><span class="sxs-lookup"><span data-stu-id="ff419-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff419-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff419-118">Return value</span></span>

<span data-ttu-id="ff419-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ff419-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff419-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff419-120">Remarks</span></span>

<span data-ttu-id="ff419-121">Questo metodo si applica solo agli elementi di tipo file.</span><span class="sxs-lookup"><span data-stu-id="ff419-121">This method applies only to file type items.</span></span> <span data-ttu-id="ff419-122">Il metodo verifica che l'elemento supporti questo metodo prima di tentare di completare il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="ff419-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="ff419-123">Usare "clipboard" come parametro *filename* per trasferire un elemento negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ff419-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="ff419-124">Impostare il valore *AsyncTransfer* su **false** per i trasferimenti all'interno di un'applicazione o di uno script in esecuzione in un ambiente che termina un processo alla fine di uno script, ad esempio Windows script host (WSH).</span><span class="sxs-lookup"><span data-stu-id="ff419-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="ff419-125">In caso contrario, lo script può terminare e il processo viene terminato prima del completamento del trasferimento.</span><span class="sxs-lookup"><span data-stu-id="ff419-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="ff419-126">Il metodo di **trasferimento** non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="ff419-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="ff419-127">Al termine di un trasferimento, questo metodo invia un evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) allo script o all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff419-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="ff419-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff419-128">Examples</span></span>

<span data-ttu-id="ff419-129">Nell'esempio seguente viene illustrato l'uso del metodo di **trasferimento** per trasferire i dati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff419-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="ff419-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff419-130">Requirements</span></span>



| <span data-ttu-id="ff419-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff419-131">Requirement</span></span> | <span data-ttu-id="ff419-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ff419-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff419-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff419-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ff419-134">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff419-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff419-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff419-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ff419-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff419-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ff419-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ff419-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff419-138"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ff419-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




