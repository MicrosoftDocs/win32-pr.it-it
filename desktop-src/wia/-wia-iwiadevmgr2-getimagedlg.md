---
description: "Il metodo IWiaDevMgr2:: GetImageDlg Visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo Windows Image Acquisition (WIA) 2,0 e di scrivere l'immagine in un file specificato."
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'Metodo IWiaDevMgr2:: GetImageDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312417"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="261e5-103">Metodo IWiaDevMgr2:: GetImageDlg</span><span class="sxs-lookup"><span data-stu-id="261e5-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="261e5-104">Il metodo **IWiaDevMgr2:: GetImageDlg** Visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo Windows Image Acquisition (WIA) 2,0 e di scrivere l'immagine in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="261e5-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="261e5-105">Questo metodo estende la funzionalità di [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) per incapsulare l'acquisizione di immagini in una singola chiamata API.</span><span class="sxs-lookup"><span data-stu-id="261e5-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="261e5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="261e5-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="261e5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="261e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261e5-108">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-109">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="261e5-109">Type: **LONG**</span></span>

<span data-ttu-id="261e5-110">Specifica il comportamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="261e5-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="261e5-111">Può essere impostato sui valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="261e5-111">Can be set to the following values:</span></span>



| <span data-ttu-id="261e5-112">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="261e5-112">Flag</span></span>                                 | <span data-ttu-id="261e5-113">Significato</span><span class="sxs-lookup"><span data-stu-id="261e5-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="261e5-114">0</span><span class="sxs-lookup"><span data-stu-id="261e5-114">0</span></span>                                    | <span data-ttu-id="261e5-115">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="261e5-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="261e5-116">\_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune</span><span class="sxs-lookup"><span data-stu-id="261e5-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="261e5-117">Utilizzare l'interfaccia utente del sistema anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="261e5-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="261e5-118">Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="261e5-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="261e5-119">Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="261e5-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="261e5-120">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="261e5-121">Type: **BSTR**</span></span>

<span data-ttu-id="261e5-122">Specifica lo scanner da usare.</span><span class="sxs-lookup"><span data-stu-id="261e5-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-123">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-124">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="261e5-124">Type: **HWND**</span></span>

<span data-ttu-id="261e5-125">Handle della finestra che possiede la finestra di dialogo **Ottieni immagine** .</span><span class="sxs-lookup"><span data-stu-id="261e5-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-126">*bstrFolderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="261e5-127">Type: **BSTR**</span></span>

<span data-ttu-id="261e5-128">Specifica il nome della cartella in cui sono archiviati i file analizzati.</span><span class="sxs-lookup"><span data-stu-id="261e5-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-129">*bstrFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="261e5-130">Type: **BSTR**</span></span>

<span data-ttu-id="261e5-131">Specifica il nome del file in cui scrivere i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="261e5-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-132">*plNumFiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-133">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="261e5-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="261e5-134">Puntatore al numero di file da analizzare.</span><span class="sxs-lookup"><span data-stu-id="261e5-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-135">_ppbstrFilePaths \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261e5-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-136">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="261e5-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="261e5-137">Indirizzo di un puntatore a una matrice di percorsi per i file analizzati.</span><span class="sxs-lookup"><span data-stu-id="261e5-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="261e5-138">Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima di chiamare **IWiaDevMgr2:: GetImageDlg** .</span><span class="sxs-lookup"><span data-stu-id="261e5-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="261e5-139">Vedere la **sezione Osservazioni**.</span><span class="sxs-lookup"><span data-stu-id="261e5-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="261e5-140">*ppItem* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="261e5-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="261e5-141">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="261e5-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="261e5-142">Indirizzo di un puntatore a [**IWiaItem2**](-wia-iwiaitem2.md) da cui sono state analizzate le immagini.</span><span class="sxs-lookup"><span data-stu-id="261e5-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="261e5-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="261e5-143">Return value</span></span>

<span data-ttu-id="261e5-144">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="261e5-144">Type: **HRESULT**</span></span>

<span data-ttu-id="261e5-145">**IWiaDevMgr2:: GetImageDlg** restituisce \_ OK se i dati vengono trasferiti correttamente, restituisce \_ false se l'utente annulla la finestra di dialogo o restituisce un errore com standard.</span><span class="sxs-lookup"><span data-stu-id="261e5-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="261e5-146">Il parametro *ppbstrFilePaths* non è necessariamente vuoto, se la funzione restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="261e5-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="261e5-147">Se l'utente Annulla, le pagine che hanno completato l'analisi vengono elaborate e restituite in *ppbstrFilePaths*.</span><span class="sxs-lookup"><span data-stu-id="261e5-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="261e5-148">Anche se non vengono usati, è necessario liberare la matrice.</span><span class="sxs-lookup"><span data-stu-id="261e5-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="261e5-149">Vedere la **sezione Osservazioni**.</span><span class="sxs-lookup"><span data-stu-id="261e5-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="261e5-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="261e5-150">Remarks</span></span>

<span data-ttu-id="261e5-151">Se l'applicazione passa **null** come valore del parametro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** Visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare il dispositivo di input WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="261e5-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="261e5-152">Usare una voce di menu denominata **da scanner** nel menu **file** per fare in modo che le selezioni del dispositivo e dell'immagine siano disponibili nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="261e5-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="261e5-153">Chiamare [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) per ogni BSTR nella matrice a cui  \[ punta ppbstrFilePaths \] e chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) sulla matrice stessa per liberare la memoria associata.</span><span class="sxs-lookup"><span data-stu-id="261e5-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="261e5-154">Se \_ viene restituito S false, verificare se il valore a cui punta *plNumFiles* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="261e5-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="261e5-155">Se il valore è diverso da zero, liberare le risorse *ppbstrFilePaths* \[ i \] nell'applicazione, in quanto l'utente può annullare l'operazione dopo aver analizzato una o più pagine.</span><span class="sxs-lookup"><span data-stu-id="261e5-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="261e5-156">Inizializzare *plNumFiles* su zero prima di chiamare **IWiaDevMgr2:: GetImageDlg**.</span><span class="sxs-lookup"><span data-stu-id="261e5-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="261e5-157">Se *plNumFiles* non è inizializzato su zero e un errore nell'infrastruttura com fa in modo che la funzione restituisca S \_ false prima di **IWiaDevMgr2:: GetImageDlg** viene chiamato, *plNumFiles* avrà un valore di Garbage Collection fuorviante.</span><span class="sxs-lookup"><span data-stu-id="261e5-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="261e5-158">La finestra di dialogo deve disporre di diritti sufficienti per *bstrFolderName* , in modo che sia possibile salvare i file con nomi file univoci.</span><span class="sxs-lookup"><span data-stu-id="261e5-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="261e5-159">Proteggere la cartella con un elenco di controllo di accesso (ACL) perché contiene dati utente.</span><span class="sxs-lookup"><span data-stu-id="261e5-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="261e5-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="261e5-160">Requirements</span></span>



| <span data-ttu-id="261e5-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="261e5-161">Requirement</span></span> | <span data-ttu-id="261e5-162">Valore</span><span class="sxs-lookup"><span data-stu-id="261e5-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="261e5-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="261e5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="261e5-164">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="261e5-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="261e5-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="261e5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="261e5-166">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="261e5-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="261e5-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="261e5-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="261e5-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="261e5-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
