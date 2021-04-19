---
description: La \_ Proprietà pkey AudioEndpoint \_ GUID fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo dell'endpoint audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305150"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="9ec35-103">\_GUID AUDIOENDPOINT \_ pkey</span><span class="sxs-lookup"><span data-stu-id="9ec35-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="9ec35-104">La proprietà **pkey \_ AudioEndpoint \_ GUID** fornisce l'identificatore di dispositivo DirectSound che corrisponde al dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="9ec35-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="9ec35-105">Il valore della proprietà è un GUID che il client può fornire come identificatore del dispositivo alla funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** nell'API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="9ec35-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="9ec35-106">Questo valore identifica in modo univoco il dispositivo dell'endpoint audio in tutti i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9ec35-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="9ec35-107">Per ulteriori informazioni su DirectSound, vedere la documentazione di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="9ec35-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="9ec35-108">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="9ec35-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="9ec35-109">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null contenente un GUID che identifica il dispositivo dell'endpoint audio in DirectSound.</span><span class="sxs-lookup"><span data-stu-id="9ec35-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="9ec35-110">Come spiegato in precedenza, l' [API MMDevice](mmdevice-api.md) supporta i [ruoli del dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9ec35-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="9ec35-111">Sebbene DirectSound non supporti direttamente i ruoli del dispositivo, un client DirectSound può utilizzare la \_ Proprietà pkey AudioEndpoint \_ GUID per selezionare un dispositivo di rendering o acquisizione DirectSound basato sul relativo ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ec35-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="9ec35-112">Ad esempio, un'applicazione DirectSound esegue i passaggi seguenti per creare un dispositivo DirectSound che corrisponde al dispositivo dell'endpoint di rendering a cui l'utente ha assegnato il ruolo eMultimedia:</span><span class="sxs-lookup"><span data-stu-id="9ec35-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="9ec35-113">Chiamare il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo dell'endpoint di rendering con il ruolo eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="9ec35-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="9ec35-114">Chiamare il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) per ottenere l'interfaccia **IPropertyStore** del dispositivo eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="9ec35-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="9ec35-115">Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9ec35-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="9ec35-116">Chiamare il metodo **IPropertyStore:: GetValue** per ottenere il \_ valore della proprietà pkey AudioEndpoint \_ GUID.</span><span class="sxs-lookup"><span data-stu-id="9ec35-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="9ec35-117">Converte il valore della proprietà da un GUID in formato stringa a una struttura GUID a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="9ec35-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="9ec35-118">Chiamare la funzione **DirectSoundCreate** con il GUID per creare il dispositivo con il ruolo eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="9ec35-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="9ec35-119">**Pkey \_ Il \_ GUID AudioEndpoint** è una proprietà di sola lettura indipendentemente dalla modalità di accesso all'archiviazione richiesta dall'applicazione in [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span><span class="sxs-lookup"><span data-stu-id="9ec35-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="9ec35-120">Se un'applicazione tenta di impostare un valore utilizzando **IPropertyStore:: SetValue**, questa chiamata ha esito negativo con il \_ codice di errore E AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="9ec35-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="9ec35-121">Si noti che il GUID a 16 byte generato nel passaggio 4 corrisponde al GUID del dispositivo che identifica il dispositivo durante l'enumerazione del dispositivo DirectSound.</span><span class="sxs-lookup"><span data-stu-id="9ec35-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="9ec35-122">La funzione **DirectSoundEnumerate** enumera i dispositivi endpoint di rendering e la funzione **DirectSoundCaptureEnumerate** enumera i dispositivi dell'endpoint di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9ec35-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="9ec35-123">In entrambi i casi, il GUID del dispositivo è il primo parametro passato alla funzione di callback di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9ec35-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="9ec35-124">Per ulteriori informazioni sull'enumerazione DirectSound, vedere la documentazione di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="9ec35-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="9ec35-125">Per un esempio di codice che usa la \_ proprietà GUID AudioEndpoint di pkey \_ , vedere [ruoli del dispositivo per le applicazioni DirectSound](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9ec35-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec35-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ec35-126">Requirements</span></span>



| <span data-ttu-id="9ec35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec35-127">Requirement</span></span> | <span data-ttu-id="9ec35-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9ec35-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec35-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ec35-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec35-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ec35-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ec35-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ec35-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec35-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ec35-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ec35-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ec35-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec35-134"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec35-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec35-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ec35-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec35-136">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="9ec35-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="9ec35-137">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="9ec35-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




