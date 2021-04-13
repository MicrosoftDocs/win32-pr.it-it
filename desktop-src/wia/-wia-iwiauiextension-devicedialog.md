---
description: Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Metodo IWiaUIExtension::D eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526448"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="c9b79-103">IWiaUIExtension::D Metodo eviceDialog</span><span class="sxs-lookup"><span data-stu-id="c9b79-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="c9b79-104">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="c9b79-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9b79-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="c9b79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b79-107">*pDeviceDialogData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9b79-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b79-108">Tipo: \**PDEVICEDIALOGDATA \** _</span><span class="sxs-lookup"><span data-stu-id="c9b79-108">Type: \**PDEVICEDIALOGDATA\** _</span></span>

<span data-ttu-id="c9b79-109">Punta a una struttura [_ *DEVICEDIALOGDATA* \*](-wia-devicedialogdata.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9b79-109">Points to a [_ *DEVICEDIALOGDATA*\*](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b79-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9b79-110">Return value</span></span>

<span data-ttu-id="c9b79-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9b79-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c9b79-112">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9b79-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c9b79-113">Se l'utente annulla la finestra di dialogo, il metodo restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="c9b79-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="c9b79-114">Se il metodo non è implementato, restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c9b79-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="c9b79-115">Se il metodo ha esito negativo, viene restituito un codice di errore COM standard.</span><span class="sxs-lookup"><span data-stu-id="c9b79-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b79-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9b79-116">Remarks</span></span>

<span data-ttu-id="c9b79-117">Se si implementa l'interfaccia [**IWiaUIExtension**](-wia-iwiauiextension.md) e non si desidera sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve eseguire alcuna operazione oltre a restituire e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c9b79-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b79-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9b79-118">Requirements</span></span>



| <span data-ttu-id="c9b79-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b79-119">Requirement</span></span> | <span data-ttu-id="c9b79-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c9b79-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b79-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9b79-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b79-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9b79-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c9b79-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9b79-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b79-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9b79-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c9b79-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9b79-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b79-126"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b79-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




