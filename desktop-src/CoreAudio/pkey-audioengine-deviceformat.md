---
description: La \_ Proprietà pkey Audioengine \_ DeviceFormat specifica il formato del dispositivo, che è il formato selezionato dall'utente per il flusso che scorre tra il motore audio e il dispositivo dell'endpoint audio quando il dispositivo funziona in modalità condivisa.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748903"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="560f7-103">PKEY \_ Audioengine \_ DeviceFormat</span><span class="sxs-lookup"><span data-stu-id="560f7-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="560f7-104">La proprietà **pkey \_ Audioengine \_ DeviceFormat** specifica il formato del dispositivo, che è il formato selezionato dall'utente per il flusso che scorre tra il motore audio e il dispositivo dell'endpoint audio quando il dispositivo funziona in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="560f7-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="560f7-105">Questo formato potrebbe non essere il formato predefinito migliore per l'uso da parte di un'applicazione in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="560f7-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="560f7-106">In genere, un'applicazione in modalità esclusiva trova un formato di dispositivo appropriato effettuando un certo numero di chiamate al metodo [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="560f7-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="560f7-107">Per altre informazioni, vedere [formati di dispositivo](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="560f7-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="560f7-108">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="560f7-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="560f7-109">Il membro **BLOB** della struttura **PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri.</span><span class="sxs-lookup"><span data-stu-id="560f7-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="560f7-110">Member **BLOB. cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato.</span><span class="sxs-lookup"><span data-stu-id="560f7-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="560f7-111">Il membro **BLOB. pBlobData** punta a una struttura **WAVEFORMATEX** che contiene la descrizione del formato.</span><span class="sxs-lookup"><span data-stu-id="560f7-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="560f7-112">Per ulteriori informazioni su **BLOB**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="560f7-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="560f7-113">Per ulteriori informazioni su **WAVEFORMATEX**, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="560f7-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="560f7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="560f7-114">Requirements</span></span>



| <span data-ttu-id="560f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="560f7-115">Requirement</span></span> | <span data-ttu-id="560f7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="560f7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="560f7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="560f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="560f7-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="560f7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="560f7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="560f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="560f7-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="560f7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="560f7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="560f7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="560f7-122"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="560f7-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="560f7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="560f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560f7-124">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="560f7-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="560f7-125">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="560f7-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




