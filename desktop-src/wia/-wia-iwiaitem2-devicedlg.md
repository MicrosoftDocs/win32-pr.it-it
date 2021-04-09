---
description: Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: Metodo IWiaItem2::D eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129430"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="50e59-103">IWiaItem2::D Metodo eviceDlg</span><span class="sxs-lookup"><span data-stu-id="50e59-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="50e59-104">Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="50e59-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e59-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50e59-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="50e59-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e59-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="50e59-108">Type: **LONG**</span></span>

<span data-ttu-id="50e59-109">Specifica un set di flag che controllano l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="50e59-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="50e59-110">Il valore può essere 0 per rappresentare il comportamento predefinito o uno dei \_ flag della finestra di dialogo del dispositivo WIA \_ descritti in [**WiaFlag**](-wia-wiaflag.md).</span><span class="sxs-lookup"><span data-stu-id="50e59-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="50e59-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="50e59-112">Type: **HWND**</span></span>

<span data-ttu-id="50e59-113">Handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="50e59-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-114">*bstrFolderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="50e59-115">Type: **BSTR**</span></span>

<span data-ttu-id="50e59-116">Specifica il nome della cartella in cui devono essere trasferiti i file.</span><span class="sxs-lookup"><span data-stu-id="50e59-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-117">*bstrFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="50e59-118">Type: **BSTR**</span></span>

<span data-ttu-id="50e59-119">Specifica il nome del file modello.</span><span class="sxs-lookup"><span data-stu-id="50e59-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-120">*plNumFiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e59-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-121">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="50e59-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="50e59-122">Puntatore al numero di elementi nella matrice _ppbstrFilePaths \*.</span><span class="sxs-lookup"><span data-stu-id="50e59-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-123">*ppbstrFilePaths* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="50e59-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-124">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="50e59-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="50e59-125">Indirizzo di un puntatore a una matrice di percorsi per i file analizzati.</span><span class="sxs-lookup"><span data-stu-id="50e59-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="50e59-126">Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima di **IWiaItem2::D evicedlg** viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="50e59-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="50e59-127">*ppIWiaItem2* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="50e59-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e59-128">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="50e59-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="50e59-129">Indirizzo di una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="50e59-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e59-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50e59-130">Return value</span></span>

<span data-ttu-id="50e59-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="50e59-131">Type: **HRESULT**</span></span>

<span data-ttu-id="50e59-132">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50e59-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50e59-133">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50e59-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e59-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="50e59-134">Remarks</span></span>

<span data-ttu-id="50e59-135">Questo metodo Visualizza una finestra di dialogo per l'utente che viene utilizzata da un'applicazione per raccogliere tutte le informazioni necessarie per l'acquisizione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="50e59-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="50e59-136">Viene anche usato per specificare le proprietà di analisi dell'immagine, ad esempio luminosità e contrasto.</span><span class="sxs-lookup"><span data-stu-id="50e59-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="50e59-137">Dopo la restituzione di questo metodo, l'applicazione può utilizzare l'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) per acquisire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="50e59-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="50e59-138">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per ogni elemento nella matrice di puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="50e59-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="50e59-139">Le applicazioni devono inoltre liberare la matrice utilizzando [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="50e59-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="50e59-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50e59-140">Requirements</span></span>



| <span data-ttu-id="50e59-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e59-141">Requirement</span></span> | <span data-ttu-id="50e59-142">Valore</span><span class="sxs-lookup"><span data-stu-id="50e59-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50e59-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50e59-143">Minimum supported client</span></span><br/> | <span data-ttu-id="50e59-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50e59-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50e59-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50e59-145">Minimum supported server</span></span><br/> | <span data-ttu-id="50e59-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50e59-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50e59-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50e59-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e59-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e59-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="50e59-149">IDL</span><span class="sxs-lookup"><span data-stu-id="50e59-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50e59-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50e59-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
