---
description: "Metodo IWiaDevMgr2::SelectDeviceDlgID: visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine."
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: Metodo IWiaDevMgr2::SelectDeviceDlgID (Wia.h)
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
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106819"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="cf950-103">Metodo IWiaDevMgr2::SelectDeviceDlgID</span><span class="sxs-lookup"><span data-stu-id="cf950-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="cf950-104">Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cf950-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf950-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf950-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="cf950-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf950-107">*hwndParent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cf950-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf950-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="cf950-108">Type: **HWND**</span></span>

<span data-ttu-id="cf950-109">Specifica la finestra padre della finestra **di dialogo Seleziona** dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf950-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="cf950-110">*lDeviceType* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cf950-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf950-111">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="cf950-111">Type: **LONG**</span></span>

<span data-ttu-id="cf950-112">Specifica il tipo di dispositivo WIA 2.0 da usare.</span><span class="sxs-lookup"><span data-stu-id="cf950-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="cf950-113">Per un elenco dei valori possibili, vedere Identificatori di tipo di dispositivo [WIA.](-wia-wia-device-type-specifiers.md)</span><span class="sxs-lookup"><span data-stu-id="cf950-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="cf950-114">*lFlags* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cf950-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf950-115">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="cf950-115">Type: **LONG**</span></span>

<span data-ttu-id="cf950-116">Specifica il comportamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="cf950-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="cf950-117">Il valore può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="cf950-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cf950-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="cf950-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cf950-119">Usare il comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="cf950-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="cf950-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cf950-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="cf950-121">Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cf950-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cf950-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf950-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf950-123">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="cf950-123">Type: **BSTR\***</span></span>

<span data-ttu-id="cf950-124">Puntatore a una stringa che riceve la stringa dell'identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf950-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf950-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf950-125">Return value</span></span>

<span data-ttu-id="cf950-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cf950-126">Type: **HRESULT**</span></span>

<span data-ttu-id="cf950-127">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="cf950-127">This method can return one of these values.</span></span>



| <span data-ttu-id="cf950-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cf950-128">Return code</span></span>                                                                                                  | <span data-ttu-id="cf950-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf950-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf950-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf950-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="cf950-131">Il dispositivo è stato selezionato correttamente.</span><span class="sxs-lookup"><span data-stu-id="cf950-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="cf950-132"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="cf950-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="cf950-133">L'utente ha annullato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="cf950-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="cf950-134"><dt>**WIA S NO DEVICE AVAILABLE (WIA \_ S \_ NESSUN DISPOSITIVO \_ \_ DISPONIBILE)**</dt></span><span class="sxs-lookup"><span data-stu-id="cf950-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="cf950-135">Nessun dispositivo hardware WIA 2.0 corrisponde alle specifiche fornite nel *parametro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="cf950-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf950-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf950-136">Remarks</span></span>

<span data-ttu-id="cf950-137">Questo metodo crea e visualizza la finestra **di dialogo Seleziona** dispositivo in modo che l'utente possa selezionare un dispositivo WIA 2.0 per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cf950-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="cf950-138">Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2::SelectDeviceDlgID** passa la stringa dell'identificatore all'applicazione tramite il relativo *parametro pbstrDeviceID.*</span><span class="sxs-lookup"><span data-stu-id="cf950-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="cf950-139">L'applicazione può limitare i dispositivi visualizzati all'utente a tipi specifici specificando i tipi di dispositivo tramite il *parametro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="cf950-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="cf950-140">Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2::SelectDeviceDlgID** non visualizza la **finestra di dialogo** Seleziona dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf950-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="cf950-141">Passa invece la stringa dell'identificatore del dispositivo all'applicazione senza visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="cf950-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="cf950-142">È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2::SelectDeviceDlgID** per visualizzare la finestra di dialogo passando WIA SELECT DEVICE NODEFAULT come valore per il \_ \_ parametro \_ *lFlags.*</span><span class="sxs-lookup"><span data-stu-id="cf950-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="cf950-143">Se più di un dispositivo WIA 2.0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo Seleziona dispositivo in modo che l'utente possa sceglierne uno.</span><span class="sxs-lookup"><span data-stu-id="cf950-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="cf950-144">È consigliabile che le applicazioni rendono disponibile la selezione di dispositivi e immagini tramite una voce di menu denominata **Da scanner** nel menu **File.**</span><span class="sxs-lookup"><span data-stu-id="cf950-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf950-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf950-145">Requirements</span></span>



| <span data-ttu-id="cf950-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf950-146">Requirement</span></span> | <span data-ttu-id="cf950-147">Valore</span><span class="sxs-lookup"><span data-stu-id="cf950-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf950-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf950-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cf950-149">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf950-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf950-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf950-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cf950-151">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf950-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf950-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf950-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf950-153"><dt>Wia.h</dt></span><span class="sxs-lookup"><span data-stu-id="cf950-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf950-154">Idl</span><span class="sxs-lookup"><span data-stu-id="cf950-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf950-155"><dt>Wia.idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf950-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




