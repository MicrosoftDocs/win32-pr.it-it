---
description: Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'Metodo IWiaDevMgr2:: SelectDeviceDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312415"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="128d1-103">Metodo IWiaDevMgr2:: SelectDeviceDlg</span><span class="sxs-lookup"><span data-stu-id="128d1-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="128d1-104">Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="128d1-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="128d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="128d1-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="128d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="128d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128d1-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="128d1-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128d1-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="128d1-108">Type: **HWND**</span></span>

<span data-ttu-id="128d1-109">Consente di specificare la finestra padre della finestra di dialogo **Seleziona dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="128d1-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="128d1-110">*lDeviceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="128d1-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128d1-111">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="128d1-111">Type: **LONG**</span></span>

<span data-ttu-id="128d1-112">Specifica il tipo di dispositivo WIA 2,0 da usare.</span><span class="sxs-lookup"><span data-stu-id="128d1-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="128d1-113">Per un elenco di valori possibili, vedere gli [identificatori del tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="128d1-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="128d1-114">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="128d1-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128d1-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="128d1-115">Type: **LONG**</span></span>

<span data-ttu-id="128d1-116">Specifica il comportamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="128d1-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="128d1-117">Il valore può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="128d1-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="128d1-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="128d1-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="128d1-119">Usare il comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="128d1-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="128d1-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="128d1-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="128d1-121">Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="128d1-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="128d1-122">*pbstrDeviceID* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="128d1-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="128d1-123">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="128d1-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="128d1-124">Nell'output, riceve una stringa che contiene la stringa dell'identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="128d1-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="128d1-125">In fase di input, passare l'indirizzo di un puntatore se queste informazioni sono necessarie oppure _ *null*\* se non è necessario.</span><span class="sxs-lookup"><span data-stu-id="128d1-125">On input, pass the address of a pointer if this information is needed, or _ *NULL*\* if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="128d1-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="128d1-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="128d1-127">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="128d1-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="128d1-128">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice della struttura ad albero gerarchica che rappresenta il dispositivo WIA 2,0 selezionato.</span><span class="sxs-lookup"><span data-stu-id="128d1-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="128d1-129">Se non viene trovato alcun dispositivo, riceve **null**.</span><span class="sxs-lookup"><span data-stu-id="128d1-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128d1-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="128d1-130">Return value</span></span>

<span data-ttu-id="128d1-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="128d1-131">Type: **HRESULT**</span></span>

<span data-ttu-id="128d1-132">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="128d1-132">This method can return one of these values.</span></span>



| <span data-ttu-id="128d1-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="128d1-133">Return code</span></span>                                                                                                  | <span data-ttu-id="128d1-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128d1-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="128d1-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="128d1-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="128d1-136">La selezione del dispositivo è stata completata.</span><span class="sxs-lookup"><span data-stu-id="128d1-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="128d1-137"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="128d1-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="128d1-138">L'utente ha annullato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="128d1-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="128d1-139"><dt>**WIA \_ S \_ nessun \_ dispositivo \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="128d1-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="128d1-140">Nessun dispositivo hardware WIA 2,0 corrisponde alle specifiche specificate nel parametro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="128d1-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="128d1-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="128d1-141">Remarks</span></span>

<span data-ttu-id="128d1-142">Questo metodo crea e visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare un dispositivo WIA 2,0 per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="128d1-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="128d1-143">Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2:: SelectDeviceDlg** crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="128d1-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="128d1-144">Archivia un puntatore all'interfaccia **IWiaItem2** dell'elemento radice nel parametro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="128d1-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="128d1-145">L'applicazione può limitare i dispositivi visualizzati all'utente a determinati tipi specificando i tipi di dispositivo tramite il parametro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="128d1-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="128d1-146">Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2:: SelectDeviceDlg** non Visualizza la finestra di dialogo **Seleziona dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="128d1-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="128d1-147">Viene invece creato l'albero [**IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo e viene archiviato un puntatore all'interfaccia **IWiaItem2** dell'elemento radice nel parametro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="128d1-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="128d1-148">È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2:: SelectDeviceDlg** per visualizzare la finestra di dialogo specificando WIA \_ selezionare \_ Device \_ NODEFAULT come valore per il parametro *è* .</span><span class="sxs-lookup"><span data-stu-id="128d1-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="128d1-149">Se più di un dispositivo WIA 2,0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo **Seleziona dispositivo** , in modo che l'utente possa sceglierne uno.</span><span class="sxs-lookup"><span data-stu-id="128d1-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="128d1-150">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppItemRoot* .</span><span class="sxs-lookup"><span data-stu-id="128d1-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="128d1-151">È consigliabile che le applicazioni rendano disponibili la selezione del dispositivo e dell'immagine tramite una voce di menu denominata **da scanner** nel menu **file** .</span><span class="sxs-lookup"><span data-stu-id="128d1-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="128d1-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="128d1-152">Requirements</span></span>



| <span data-ttu-id="128d1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="128d1-153">Requirement</span></span> | <span data-ttu-id="128d1-154">Valore</span><span class="sxs-lookup"><span data-stu-id="128d1-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="128d1-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="128d1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="128d1-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="128d1-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="128d1-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="128d1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="128d1-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="128d1-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="128d1-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="128d1-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="128d1-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="128d1-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="128d1-161">IDL</span><span class="sxs-lookup"><span data-stu-id="128d1-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="128d1-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="128d1-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
