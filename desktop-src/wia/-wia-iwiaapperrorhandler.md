---
description: L'interfaccia IWiaAppErrorHandler consente alle applicazioni di visualizzare le finestre di errore, durante i trasferimenti di dati, da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaccia IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312420"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="4711c-103">Interfaccia IWiaAppErrorHandler</span><span class="sxs-lookup"><span data-stu-id="4711c-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="4711c-104">L'interfaccia **IWiaAppErrorHandler** consente alle applicazioni di visualizzare le finestre di errore, durante i trasferimenti di dati, da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4711c-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="4711c-105">Membri</span><span class="sxs-lookup"><span data-stu-id="4711c-105">Members</span></span>

<span data-ttu-id="4711c-106">L'interfaccia **IWiaAppErrorHandler** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4711c-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4711c-107">**IWiaAppErrorHandler** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4711c-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="4711c-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="4711c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4711c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4711c-109">Methods</span></span>

<span data-ttu-id="4711c-110">L'interfaccia **IWiaAppErrorHandler** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4711c-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="4711c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="4711c-111">Method</span></span>                                                        | <span data-ttu-id="4711c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4711c-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4711c-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="4711c-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="4711c-114">Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4711c-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="4711c-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="4711c-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="4711c-116">Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.</span><span class="sxs-lookup"><span data-stu-id="4711c-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="4711c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4711c-117">Remarks</span></span>

<span data-ttu-id="4711c-118">L'oggetto di gestione degli errori, o callback, che implementa questa interfaccia viene passato in [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) e [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).</span><span class="sxs-lookup"><span data-stu-id="4711c-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="4711c-119">Questa interfaccia non è progettata per gestire gli errori riscontrati al di fuori dei trasferimenti di dati di immagini, ad esempio errori durante il recupero o l'impostazione delle proprietà del dispositivo o callback non restituiti in un driver.</span><span class="sxs-lookup"><span data-stu-id="4711c-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="4711c-120">Un gestore degli errori del driver deve implementare [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), invece di **IWiaAppErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="4711c-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="4711c-121">L'oggetto che implementa questa interfaccia deve implementare anche [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span><span class="sxs-lookup"><span data-stu-id="4711c-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="4711c-122">Se si desidera che un gestore degli errori del driver e un gestore degli errori predefinito visualizzino le finestre dei messaggi di errore, ma non si desidera creare un gestore degli errori completo per l'applicazione, implementare questa interfaccia e implementare anche il metodo [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) per restituire \_ lo stato WIA \_ non \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="4711c-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="4711c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4711c-123">Requirements</span></span>



| <span data-ttu-id="4711c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4711c-124">Requirement</span></span> | <span data-ttu-id="4711c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4711c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4711c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4711c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4711c-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4711c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4711c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4711c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4711c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4711c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4711c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4711c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4711c-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4711c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="4711c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4711c-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
