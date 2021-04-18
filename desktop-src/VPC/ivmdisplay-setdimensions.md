---
title: Metodo sedimensions IVMDisplay (VPCCOMInterfaces. h)
description: Imposta l'altezza e la larghezza dello schermo della macchina virtuale, in pixel.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Metodo sedimensions Virtual PC
- Metodo sedimensions Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, metodo sedimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302421"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="a49ed-106">Metodo IVMDisplay:: sedimensions</span><span class="sxs-lookup"><span data-stu-id="a49ed-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="a49ed-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a49ed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a49ed-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a49ed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a49ed-109">Imposta l'altezza e la larghezza della visualizzazione della macchina virtuale (VM), in pixel.</span><span class="sxs-lookup"><span data-stu-id="a49ed-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="a49ed-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a49ed-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="a49ed-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a49ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a49ed-112">*displayPixelWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a49ed-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49ed-113">Larghezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a49ed-113">The width, in pixels.</span></span> <span data-ttu-id="a49ed-114">Il valore deve essere compreso tra i valori 640 e 2048.</span><span class="sxs-lookup"><span data-stu-id="a49ed-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="a49ed-115">Se il valore non è divisibile in modo uniforme per 8, verrà ridotto al multiplo inferiore successivo di 8.</span><span class="sxs-lookup"><span data-stu-id="a49ed-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="a49ed-116">*displayPixelHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a49ed-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49ed-117">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a49ed-117">The height, in pixels.</span></span> <span data-ttu-id="a49ed-118">Il valore deve essere compreso tra i valori 480 e 1920.</span><span class="sxs-lookup"><span data-stu-id="a49ed-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a49ed-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a49ed-119">Return value</span></span>

<span data-ttu-id="a49ed-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a49ed-120">This method can return one of these values.</span></span>



| <span data-ttu-id="a49ed-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a49ed-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="a49ed-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a49ed-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a49ed-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a49ed-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a49ed-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="a49ed-125"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a49ed-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="a49ed-126">Il parametro *displayPixelWidth* non è divisibile uniformemente per 8 oppure il parametro *displayPixelWidth* o *displayPixelHeight* non è compreso nei valori minimi consentiti (640x480) o 2048x1920 massimi.</span><span class="sxs-lookup"><span data-stu-id="a49ed-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="a49ed-127"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="a49ed-128">La modifica della risoluzione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="a49ed-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="a49ed-129"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="a49ed-130">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a49ed-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="a49ed-131"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="a49ed-132">La macchina virtuale non è valida o non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a49ed-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="a49ed-133"><dt>**Macchina virtuale \_ E \_ Nessuna \_ visualizzazione**</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="a49ed-134">Non è possibile individuare una visualizzazione valida per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a49ed-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="a49ed-135"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="a49ed-136">La versione dei componenti di integrazione installati nel sistema operativo guest non supporta questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a49ed-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="a49ed-137"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a49ed-138">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a49ed-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="a49ed-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="a49ed-139">Remarks</span></span>

<span data-ttu-id="a49ed-140">Le dimensioni minime della visualizzazione della macchina virtuale sono 640 x 480 pixel.</span><span class="sxs-lookup"><span data-stu-id="a49ed-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="a49ed-141">La dimensione massima è 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="a49ed-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="a49ed-142">Il tentativo di impostare la dimensione di visualizzazione su valori non compresi in questi limiti o su qualsiasi larghezza non divisibile per 8, comporterà la restituzione di un errore **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="a49ed-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a49ed-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a49ed-143">Requirements</span></span>



| <span data-ttu-id="a49ed-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a49ed-144">Requirement</span></span> | <span data-ttu-id="a49ed-145">Valore</span><span class="sxs-lookup"><span data-stu-id="a49ed-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49ed-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a49ed-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a49ed-147">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a49ed-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a49ed-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a49ed-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a49ed-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a49ed-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a49ed-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a49ed-150">End of client support</span></span><br/>    | <span data-ttu-id="a49ed-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a49ed-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a49ed-152">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a49ed-152">Product</span></span><br/>                  | <span data-ttu-id="a49ed-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a49ed-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a49ed-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a49ed-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a49ed-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a49ed-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a49ed-156">IID</span><span class="sxs-lookup"><span data-stu-id="a49ed-156">IID</span></span><br/>                      | <span data-ttu-id="a49ed-157">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="a49ed-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a49ed-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a49ed-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49ed-159">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="a49ed-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

