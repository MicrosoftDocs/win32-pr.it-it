---
title: Interfacce di Servizi Desktop remoto AudioEndpoint
description: Con l'API AudioEndpoint vengono usate le interfacce seguenti.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298031"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="ca13c-103">Interfacce di Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca13c-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="ca13c-104">Con l'API AudioEndpoint vengono usate le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca13c-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca13c-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ca13c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ca13c-106">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ca13c-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="ca13c-107">Inizializza un oggetto endpoint dispositivo e ottiene le funzionalità del dispositivo che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="ca13c-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="ca13c-108">**IAudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ca13c-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="ca13c-109">Fornisce informazioni al motore audio di un endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="ca13c-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="ca13c-110">Questa interfaccia viene implementata da un endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="ca13c-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="ca13c-111">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="ca13c-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="ca13c-112">Controlla lo stato del flusso di un endpoint.</span><span class="sxs-lookup"><span data-stu-id="ca13c-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="ca13c-113">**IAudioEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ca13c-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="ca13c-114">Ottiene la differenza tra le posizioni di lettura e scrittura correnti nel buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ca13c-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="ca13c-115">**IAudioInputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ca13c-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="ca13c-116">Ottiene il buffer di input per ogni passaggio di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ca13c-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="ca13c-117">**IAudioOutputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ca13c-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="ca13c-118">Ottiene il buffer di output per ogni passaggio di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ca13c-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca13c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca13c-119">Remarks</span></span>

<span data-ttu-id="ca13c-120">L'API Servizi Desktop remoto AudioEndpoint è destinata all'uso in scenari Desktop remoto; non è per le applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="ca13c-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




