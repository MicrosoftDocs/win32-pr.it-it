---
description: Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Metodo IWiaAppErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308245"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="6133b-103">Metodo IWiaAppErrorHandler:: ReportStatus</span><span class="sxs-lookup"><span data-stu-id="6133b-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="6133b-104">Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.</span><span class="sxs-lookup"><span data-stu-id="6133b-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6133b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6133b-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="6133b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6133b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6133b-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6133b-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6133b-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="6133b-108">Type: **LONG**</span></span>

<span data-ttu-id="6133b-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6133b-109">Not used.</span></span> <span data-ttu-id="6133b-110">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="6133b-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6133b-111">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6133b-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6133b-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="6133b-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="6133b-113">Puntatore all'elemento da trasferire.</span><span class="sxs-lookup"><span data-stu-id="6133b-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="6133b-114">_hrStatus \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6133b-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6133b-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6133b-115">Type: **HRESULT**</span></span>

<span data-ttu-id="6133b-116">Codice di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6133b-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="6133b-117">*lPercentComplete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6133b-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6133b-118">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="6133b-118">Type: **LONG**</span></span>

<span data-ttu-id="6133b-119">Percentuale di completamento dell'operazione corrente.</span><span class="sxs-lookup"><span data-stu-id="6133b-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6133b-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6133b-120">Return value</span></span>

<span data-ttu-id="6133b-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6133b-121">Type: **HRESULT**</span></span>

<span data-ttu-id="6133b-122">Restituisce *hrStatus* se non è possibile recuperare l'errore.</span><span class="sxs-lookup"><span data-stu-id="6133b-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="6133b-123">In caso contrario, restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6133b-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="6133b-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6133b-124">Return code</span></span>                                                                                              | <span data-ttu-id="6133b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6133b-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6133b-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="6133b-127">Se *hrStatus* è un errore, è stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare.</span><span class="sxs-lookup"><span data-stu-id="6133b-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="6133b-128">Se *hrStatus* è informativo, l'utente è stato informato con una finestra di dialogo non modale e ha scelto di non annullare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6133b-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="6133b-129"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="6133b-130">L'utente ha annullato il trasferimento dalla finestra di dialogo non modale del gestore errori.</span><span class="sxs-lookup"><span data-stu-id="6133b-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="6133b-131">Questo valore può essere restituito in qualsiasi momento, a prescindere dal tipo di *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="6133b-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="6133b-132"><dt>**\_stato WIA \_ non \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="6133b-133">Non è stata eseguita alcuna azione. ovvero, nessuna finestra di dialogo è stata presentata all'utente.</span><span class="sxs-lookup"><span data-stu-id="6133b-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="6133b-134">Verrà richiamato il gestore degli errori successivo.</span><span class="sxs-lookup"><span data-stu-id="6133b-134">The next error handler will be invoked.</span></span> <span data-ttu-id="6133b-135">L'ordine dei gestori di errori è: applicazione, driver e impostazione predefinita del sistema.</span><span class="sxs-lookup"><span data-stu-id="6133b-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="6133b-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="6133b-136">Remarks</span></span>

<span data-ttu-id="6133b-137">Il parametro *lPercentComplete* consente a una finestra del gestore errori di visualizzare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="6133b-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="6133b-138">Un driver, ad esempio, potrebbe fornire una stima del tempo necessario per il "riscaldamento".</span><span class="sxs-lookup"><span data-stu-id="6133b-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="6133b-139">Il parametro *lPercentComplete* passato a **IWiaAppErrorHandler:: ReportStatus** è uguale al valore di **lPercentComplete** impostato dal driver nella struttura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="6133b-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="6133b-140">Un gestore degli errori può usare le macro SUCCEEDed e FAILED per verificare se *hrStatus* ha un errore di gravità o la gravità è riuscita \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6133b-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="6133b-141">Se *hrStatus* ha \_ esito positivo, l'utente deve essere autorizzato a annullare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="6133b-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="6133b-142">Se *hrStatus* è \_ un errore di gravità, il gestore degli errori dovrebbe visualizzare una finestra di dialogo modale di proprietà della finestra padre dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6133b-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6133b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6133b-143">Requirements</span></span>



| <span data-ttu-id="6133b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6133b-144">Requirement</span></span> | <span data-ttu-id="6133b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="6133b-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6133b-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6133b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6133b-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6133b-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6133b-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6133b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6133b-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6133b-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6133b-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6133b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6133b-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="6133b-152">IDL</span><span class="sxs-lookup"><span data-stu-id="6133b-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6133b-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="6133b-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="6133b-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="6133b-155"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6133b-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




