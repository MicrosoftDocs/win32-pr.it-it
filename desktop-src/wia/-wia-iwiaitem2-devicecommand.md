---
description: Invia un comando a un dispositivo hardware Windows Image Acquisition (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: Metodo IWiaItem2::D eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307366"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="85cfc-103">IWiaItem2::D Metodo eviceCommand</span><span class="sxs-lookup"><span data-stu-id="85cfc-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="85cfc-104">Invia un comando a un dispositivo hardware Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="85cfc-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85cfc-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="85cfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cfc-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85cfc-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cfc-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="85cfc-108">Type: **LONG**</span></span>

<span data-ttu-id="85cfc-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="85cfc-109">Currently unused.</span></span> <span data-ttu-id="85cfc-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="85cfc-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="85cfc-111">*pCmdGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85cfc-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cfc-112">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="85cfc-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="85cfc-113">Specifica il comando da inviare al dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="85cfc-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="85cfc-114">Vedere [_ *comandi* \* del dispositivo WIA](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="85cfc-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="85cfc-115">*ppIWiaItem2* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="85cfc-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cfc-116">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="85cfc-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="85cfc-117">Riceve l'indirizzo di un puntatore all'elemento [**IWiaItem2**](-wia-iwiaitem2.md) creato dal comando, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="85cfc-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cfc-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85cfc-118">Return value</span></span>

<span data-ttu-id="85cfc-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85cfc-119">Type: **HRESULT**</span></span>

<span data-ttu-id="85cfc-120">Oltre ai codici di errore COM standard, il metodo può restituire il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="85cfc-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="85cfc-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="85cfc-121">Return code</span></span>                                                                                       | <span data-ttu-id="85cfc-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85cfc-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85cfc-123"><dt>**E \_ CMDNOTSUPPORTED**</dt></span><span class="sxs-lookup"><span data-stu-id="85cfc-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="85cfc-124">Il comando non è implementato per l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) in cui viene chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="85cfc-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="85cfc-125">Il valore numerico per questo errore non è ancora definito.</span><span class="sxs-lookup"><span data-stu-id="85cfc-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="85cfc-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="85cfc-126">Remarks</span></span>

<span data-ttu-id="85cfc-127">Il comportamento di questo metodo è diverso a seconda della categoria del nodo in cui viene chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="85cfc-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="85cfc-128">Quando l'applicazione invia il comando [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) al dispositivo usando il metodo **IWiaItem2::D EVICECOMMAND** , il sistema di runtime WIA 2,0 crea un oggetto [**IWiaItem2**](-wia-iwiaitem2.md) per rappresentare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="85cfc-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="85cfc-129">Il metodo **IWiaItem2::D evicecommand** archivia l'indirizzo dell'interfaccia nel parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="85cfc-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="85cfc-130">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="85cfc-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="85cfc-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85cfc-131">Requirements</span></span>



| <span data-ttu-id="85cfc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cfc-132">Requirement</span></span> | <span data-ttu-id="85cfc-133">Valore</span><span class="sxs-lookup"><span data-stu-id="85cfc-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85cfc-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85cfc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="85cfc-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85cfc-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85cfc-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85cfc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="85cfc-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85cfc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85cfc-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85cfc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="85cfc-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="85cfc-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="85cfc-140">IDL</span><span class="sxs-lookup"><span data-stu-id="85cfc-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85cfc-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85cfc-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
