---
description: "Metodo IWiaUIExtension::D eviceDialog: fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita."
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Metodo IWiaUIExtension::D eviceDialog (Wiadevd.h)
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
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116709"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="a5c0b-103">Metodo IWiaUIExtension::D eviceDialog</span><span class="sxs-lookup"><span data-stu-id="a5c0b-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="a5c0b-104">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5c0b-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="a5c0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c0b-107">*pDeviceDialogData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a5c0b-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c0b-108">Tipo: **PDEVICEDIALOGDATA \***</span><span class="sxs-lookup"><span data-stu-id="a5c0b-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="a5c0b-109">Punta a una [**struttura DEVICEDIALOGDATA**](-wia-devicedialogdata.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c0b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5c0b-110">Return value</span></span>

<span data-ttu-id="a5c0b-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a5c0b-111">Type: **HRESULT**</span></span>

<span data-ttu-id="a5c0b-112">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="a5c0b-113">Se l'utente annulla la finestra di dialogo, il metodo restituisce S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="a5c0b-114">Se il metodo non è implementato, restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="a5c0b-115">Se il metodo ha esito negativo, restituisce un codice di errore COM standard.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c0b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5c0b-116">Remarks</span></span>

<span data-ttu-id="a5c0b-117">Se si implementa [**l'interfaccia IWiaUIExtension**](-wia-iwiauiextension.md) e non si vuole sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve fare altro che restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a5c0b-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c0b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5c0b-118">Requirements</span></span>



| <span data-ttu-id="a5c0b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c0b-119">Requirement</span></span> | <span data-ttu-id="a5c0b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a5c0b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c0b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5c0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c0b-122">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a5c0b-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a5c0b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5c0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c0b-124">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5c0b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5c0b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5c0b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5c0b-126"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c0b-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




