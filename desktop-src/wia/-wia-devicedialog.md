---
description: Utilizzato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Funzione DeviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312442"
---
# <a name="devicedialog-function"></a><span data-ttu-id="72ff0-103">DeviceDialog (funzione)</span><span class="sxs-lookup"><span data-stu-id="72ff0-103">DeviceDialog function</span></span>

<span data-ttu-id="72ff0-104">Utilizzato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.</span><span class="sxs-lookup"><span data-stu-id="72ff0-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ff0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72ff0-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="72ff0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72ff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ff0-107">*pDeviceDialogData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72ff0-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ff0-108">Tipo: **PDEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="72ff0-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="72ff0-109">[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) da usare per creare la finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72ff0-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ff0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72ff0-110">Return value</span></span>

<span data-ttu-id="72ff0-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="72ff0-111">Type: **HRESULT**</span></span>

<span data-ttu-id="72ff0-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72ff0-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72ff0-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72ff0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="72ff0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72ff0-114">Requirements</span></span>



| <span data-ttu-id="72ff0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ff0-115">Requirement</span></span> | <span data-ttu-id="72ff0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="72ff0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72ff0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72ff0-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72ff0-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="72ff0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72ff0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72ff0-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72ff0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72ff0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72ff0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72ff0-122"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="72ff0-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="72ff0-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="72ff0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="72ff0-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72ff0-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ff0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72ff0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ff0-126">**DEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="72ff0-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




