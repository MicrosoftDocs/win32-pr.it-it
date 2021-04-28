---
description: "Metodo IWiaUIExtension2::D eviceDialog: fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita."
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Metodo IWiaUIExtension2::D eviceDialog (Wiadevd.h)
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
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116649"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="f0137-103">Metodo IWiaUIExtension2::D eviceDialog</span><span class="sxs-lookup"><span data-stu-id="f0137-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="f0137-104">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="f0137-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0137-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0137-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="f0137-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0137-107">*pDeviceDialogData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0137-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0137-108">Tipo: **PDEVICEDIALOGDATA2 \***</span><span class="sxs-lookup"><span data-stu-id="f0137-108">Type: **PDEVICEDIALOGDATA2\***</span></span>

<span data-ttu-id="f0137-109">Punta a una [**struttura DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0137-109">Points to a [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0137-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0137-110">Return value</span></span>

<span data-ttu-id="f0137-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0137-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f0137-112">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0137-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f0137-113">Se l'utente annulla la finestra di dialogo, il metodo restituisce S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="f0137-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="f0137-114">Se il metodo ha esito negativo, restituisce un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="f0137-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="f0137-115">La tabella seguente illustra alcuni dei possibili codici di stato restituiti.</span><span class="sxs-lookup"><span data-stu-id="f0137-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="f0137-116">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="f0137-116">Error code</span></span>    | <span data-ttu-id="f0137-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0137-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="f0137-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f0137-118">E\_INVALIDARG</span></span> | <span data-ttu-id="f0137-119">Il parametro pDeviceDialogData è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f0137-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="f0137-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f0137-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="f0137-121">Il metodo non è implementato.</span><span class="sxs-lookup"><span data-stu-id="f0137-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="f0137-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0137-122">Remarks</span></span>

<span data-ttu-id="f0137-123">Se si implementa [**l'interfaccia IWiaUIExtension2**](-wia-iwiauiextension2.md) e non si vuole sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve fare altro che restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f0137-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0137-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0137-124">Requirements</span></span>



| <span data-ttu-id="f0137-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0137-125">Requirement</span></span> | <span data-ttu-id="f0137-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f0137-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0137-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0137-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0137-128">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0137-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f0137-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0137-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0137-130">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0137-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f0137-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0137-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0137-132"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="f0137-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




