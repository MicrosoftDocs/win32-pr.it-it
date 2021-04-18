---
description: Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Metodo IWiaAppErrorHandler:: GetWindow (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312423"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="4aa8f-103">Metodo IWiaAppErrorHandler:: GetWindow</span><span class="sxs-lookup"><span data-stu-id="4aa8f-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="4aa8f-104">Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4aa8f-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="4aa8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4aa8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa8f-107">*phwnd* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4aa8f-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa8f-108">Tipo: \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="4aa8f-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="4aa8f-109">HWND utilizzato dal gestore degli errori dell'applicazione, dal gestore degli errori del driver e dal gestore degli errori predefinito per le finestre di dialogo del messaggio del dispositivo (sia errore che informativo).</span><span class="sxs-lookup"><span data-stu-id="4aa8f-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="4aa8f-110">Il valore di output può essere _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa8f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4aa8f-111">Return value</span></span>

<span data-ttu-id="4aa8f-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4aa8f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="4aa8f-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4aa8f-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4aa8f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa8f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4aa8f-115">Remarks</span></span>

<span data-ttu-id="4aa8f-116">*phwnd* punta alla finestra passata in [**REPORTSTATUS**](-wia-iwiaerrorhandler-reportstatus.md) dal proxy WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="4aa8f-117">Questa finestra deve rimanere valida per la durata del trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa8f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aa8f-118">Requirements</span></span>



| <span data-ttu-id="4aa8f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa8f-119">Requirement</span></span> | <span data-ttu-id="4aa8f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4aa8f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa8f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa8f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa8f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4aa8f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4aa8f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa8f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa8f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4aa8f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4aa8f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4aa8f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aa8f-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa8f-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="4aa8f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="4aa8f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4aa8f-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4aa8f-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="4aa8f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="4aa8f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4aa8f-130"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4aa8f-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




