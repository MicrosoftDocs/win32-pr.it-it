---
description: Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Metodo IWiaUIExtension2::D eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226143"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="9db50-103">IWiaUIExtension2::D Metodo eviceDialog</span><span class="sxs-lookup"><span data-stu-id="9db50-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="9db50-104">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="9db50-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db50-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9db50-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="9db50-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9db50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db50-107">*pDeviceDialogData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9db50-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db50-108">Tipo: \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="9db50-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="9db50-109">Punta a una struttura [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9db50-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db50-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9db50-110">Return value</span></span>

<span data-ttu-id="9db50-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9db50-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9db50-112">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9db50-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9db50-113">Se l'utente annulla la finestra di dialogo, il metodo restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="9db50-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="9db50-114">Se il metodo ha esito negativo, viene restituito un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="9db50-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="9db50-115">Nella tabella seguente vengono illustrati alcuni dei possibili codici di stato restituiti.</span><span class="sxs-lookup"><span data-stu-id="9db50-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="9db50-116">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="9db50-116">Error code</span></span>    | <span data-ttu-id="9db50-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db50-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="9db50-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9db50-118">E\_INVALIDARG</span></span> | <span data-ttu-id="9db50-119">Il parametro pDeviceDialogData è **null**.</span><span class="sxs-lookup"><span data-stu-id="9db50-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="9db50-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9db50-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="9db50-121">Il metodo non è implementato.</span><span class="sxs-lookup"><span data-stu-id="9db50-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="9db50-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9db50-122">Remarks</span></span>

<span data-ttu-id="9db50-123">Se si implementa l'interfaccia [**IWiaUIExtension2**](-wia-iwiauiextension2.md) e non si desidera sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve eseguire alcuna operazione oltre a restituire e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9db50-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db50-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9db50-124">Requirements</span></span>



| <span data-ttu-id="9db50-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db50-125">Requirement</span></span> | <span data-ttu-id="9db50-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9db50-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9db50-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db50-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9db50-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9db50-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9db50-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db50-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9db50-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9db50-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9db50-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9db50-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db50-132"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db50-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




