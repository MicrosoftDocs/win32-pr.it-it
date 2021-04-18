---
description: Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Metodo IWiaErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312399"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="32538-103">Metodo IWiaErrorHandler:: ReportStatus</span><span class="sxs-lookup"><span data-stu-id="32538-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="32538-104">Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.</span><span class="sxs-lookup"><span data-stu-id="32538-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="32538-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32538-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="32538-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32538-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32538-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32538-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32538-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="32538-108">Type: **HWND**</span></span>

<span data-ttu-id="32538-109">**HWND** che rappresenta la finestra padre della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="32538-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="32538-110">*punkItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32538-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32538-111">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="32538-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="32538-112">Puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire.</span><span class="sxs-lookup"><span data-stu-id="32538-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="32538-113">Questo oggetto implementa almeno [_ *IWiaItem2* \*](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="32538-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="32538-114">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32538-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32538-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="32538-115">Type: **HRESULT**</span></span>

<span data-ttu-id="32538-116">**HRESULT** che rappresenta il codice di stato ricevuto da [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="32538-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="32538-117">*cbResLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32538-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32538-118">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="32538-118">Type: **LONG**</span></span>

<span data-ttu-id="32538-119">**Long** che corrisponde alla dimensione dei dati a cui fa riferimento *pbData*.</span><span class="sxs-lookup"><span data-stu-id="32538-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="32538-120">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32538-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32538-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="32538-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="32538-122">Puntatore al buffer di dati ricevuto da [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="32538-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32538-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32538-123">Return value</span></span>

<span data-ttu-id="32538-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="32538-124">Type: **HRESULT**</span></span>

<span data-ttu-id="32538-125">Restituisce *hrStatus* se l'errore non può essere recuperato da.</span><span class="sxs-lookup"><span data-stu-id="32538-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="32538-126">In caso contrario, restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32538-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="32538-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="32538-127">Return code</span></span>                                                                             | <span data-ttu-id="32538-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32538-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32538-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32538-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="32538-130">È stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare.</span><span class="sxs-lookup"><span data-stu-id="32538-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="32538-131"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="32538-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="32538-132">Non è stata eseguita alcuna azione per gestire lo stato dell'errore o del report all'utente.</span><span class="sxs-lookup"><span data-stu-id="32538-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="32538-133"><dt>**\_Interrompi E**</dt></span><span class="sxs-lookup"><span data-stu-id="32538-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="32538-134">L'utente ha scelto di interrompere il trasferimento in risposta alla finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="32538-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="32538-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="32538-135">Remarks</span></span>

<span data-ttu-id="32538-136">Windows Image Acquisition (WIA) 2,0 chiama **IWiaErrorHandler:: ReportStatus** quando il driver invia un messaggio di **\_ \_ \_ stato del dispositivo msg it** a [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="32538-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="32538-137">Questo metodo gestisce il messaggio e visualizza all'utente le informazioni sullo stato o sull'errore.</span><span class="sxs-lookup"><span data-stu-id="32538-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="32538-138">Se il messaggio riguarda un errore, il metodo consente all'utente di scegliere, se possibile, se provare a correggere l'errore e continuare il trasferimento o interrompere.</span><span class="sxs-lookup"><span data-stu-id="32538-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="32538-139">*hrStatus* è impostato su WIA \_ stato \_ trasferimento \_ inizio per informare il gestore che è stato avviato un trasferimento.</span><span class="sxs-lookup"><span data-stu-id="32538-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="32538-140">Viene impostato su WIA \_ status \_ Transfer end al termine \_ del trasferimento.</span><span class="sxs-lookup"><span data-stu-id="32538-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="32538-141">Se *hrStatus* ha \_ esito positivo, l'utente deve essere autorizzato a annullare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="32538-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="32538-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32538-142">Requirements</span></span>



| <span data-ttu-id="32538-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="32538-143">Requirement</span></span> | <span data-ttu-id="32538-144">Valore</span><span class="sxs-lookup"><span data-stu-id="32538-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32538-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32538-145">Minimum supported client</span></span><br/> | <span data-ttu-id="32538-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32538-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="32538-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32538-147">Minimum supported server</span></span><br/> | <span data-ttu-id="32538-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32538-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="32538-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32538-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="32538-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="32538-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="32538-151">IDL</span><span class="sxs-lookup"><span data-stu-id="32538-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32538-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32538-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="32538-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="32538-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="32538-154"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32538-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
