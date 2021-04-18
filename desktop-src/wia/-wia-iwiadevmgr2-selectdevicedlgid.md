---
description: Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'Metodo IWiaDevMgr2:: SelectDeviceDlgID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308233"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="a896f-103">Metodo IWiaDevMgr2:: SelectDeviceDlgID</span><span class="sxs-lookup"><span data-stu-id="a896f-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="a896f-104">Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="a896f-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a896f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a896f-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="a896f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a896f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a896f-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a896f-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a896f-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="a896f-108">Type: **HWND**</span></span>

<span data-ttu-id="a896f-109">Consente di specificare la finestra padre della finestra di dialogo **Seleziona dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="a896f-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="a896f-110">*lDeviceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a896f-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a896f-111">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="a896f-111">Type: **LONG**</span></span>

<span data-ttu-id="a896f-112">Specifica il tipo di dispositivo WIA 2,0 da usare.</span><span class="sxs-lookup"><span data-stu-id="a896f-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="a896f-113">Per un elenco di valori possibili, vedere gli [identificatori del tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="a896f-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a896f-114">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a896f-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a896f-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="a896f-115">Type: **LONG**</span></span>

<span data-ttu-id="a896f-116">Specifica il comportamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a896f-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="a896f-117">Il valore può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="a896f-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a896f-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a896f-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a896f-119">Usare il comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="a896f-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="a896f-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a896f-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="a896f-121">Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a896f-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a896f-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a896f-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a896f-123">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="a896f-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="a896f-124">Puntatore a una stringa che riceve la stringa dell'identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a896f-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a896f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a896f-125">Return value</span></span>

<span data-ttu-id="a896f-126">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a896f-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a896f-127">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a896f-127">This method can return one of these values.</span></span>



| <span data-ttu-id="a896f-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a896f-128">Return code</span></span>                                                                                                  | <span data-ttu-id="a896f-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a896f-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a896f-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a896f-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="a896f-131">La selezione del dispositivo è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a896f-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="a896f-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a896f-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="a896f-133">L'utente ha annullato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a896f-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="a896f-134"><dt>**WIA \_ S \_ nessun \_ dispositivo \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="a896f-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="a896f-135">Nessun dispositivo hardware WIA 2,0 corrisponde alle specifiche specificate nel parametro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="a896f-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a896f-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="a896f-136">Remarks</span></span>

<span data-ttu-id="a896f-137">Questo metodo crea e visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare un dispositivo WIA 2,0 per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="a896f-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="a896f-138">Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2:: SelectDeviceDlgID** passa la stringa dell'identificatore all'applicazione tramite il parametro *pbstrDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="a896f-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="a896f-139">L'applicazione può limitare i dispositivi visualizzati all'utente a determinati tipi specificando i tipi di dispositivo tramite il parametro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="a896f-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="a896f-140">Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2:: SelectDeviceDlgID** non Visualizza la finestra di dialogo **Seleziona dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="a896f-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="a896f-141">Passa invece la stringa dell'identificatore del dispositivo all'applicazione senza visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a896f-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="a896f-142">È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2:: SelectDeviceDlgID** per visualizzare la finestra di dialogo passando WIA \_ Select \_ Device \_ NODEFAULT come valore per il parametro *è* .</span><span class="sxs-lookup"><span data-stu-id="a896f-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="a896f-143">Se più di un dispositivo WIA 2,0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo SelectDevice in modo che l'utente possa sceglierne uno.</span><span class="sxs-lookup"><span data-stu-id="a896f-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="a896f-144">È consigliabile che le applicazioni rendano disponibili la selezione del dispositivo e dell'immagine tramite una voce di menu denominata **da scanner** nel menu **file** .</span><span class="sxs-lookup"><span data-stu-id="a896f-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a896f-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a896f-145">Requirements</span></span>



| <span data-ttu-id="a896f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a896f-146">Requirement</span></span> | <span data-ttu-id="a896f-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a896f-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a896f-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a896f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a896f-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a896f-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a896f-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a896f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a896f-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a896f-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a896f-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a896f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a896f-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a896f-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a896f-154">IDL</span><span class="sxs-lookup"><span data-stu-id="a896f-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a896f-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a896f-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




