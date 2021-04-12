---
title: Specifica delle azioni da eseguire
description: Specifica delle azioni da eseguire
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- ASF (Advanced Systems Format), specifica di azioni
- ASF (Advanced Systems Format), specifica di azioni
- Digital Rights Management (DRM), specifica di azioni
- DRM (Digital Rights Management), specifica di azioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398608"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="47998-107">Specifica delle azioni da eseguire</span><span class="sxs-lookup"><span data-stu-id="47998-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="47998-108">Quando si chiama prima [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) per creare l'oggetto Reader, il secondo parametro è **un operatore OR** bit per bit di valori di [**\_ diritti WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="47998-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="47998-109">Utilizzare questo parametro per specificare le azioni che verranno intraprese dall'applicazione sul primo file da aprire.</span><span class="sxs-lookup"><span data-stu-id="47998-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="47998-110">Queste azioni corrispondono direttamente ai diritti che è possibile specificare nella licenza.</span><span class="sxs-lookup"><span data-stu-id="47998-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="47998-111">Nelle chiamate successive a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)è possibile modificare i diritti richiesti chiamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specificando la costante definita per la proprietà [**\_ Rights DRM**](drm-rights.md) e usando i valori letterali stringa (di tipo **WCHAR**) separati da punto e virgola per identificare i diritti.</span><span class="sxs-lookup"><span data-stu-id="47998-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="47998-112">Il frammento di codice seguente richiede quattro diritti: riprodurre il file, copiarlo in un dispositivo e riprodurlo come parte di una playlist collaborativa.</span><span class="sxs-lookup"><span data-stu-id="47998-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="47998-113">Non confondere la [**proprietà \_ dei diritti DRM**](drm-rights.md) con la proprietà dei [**\_ flag DRM**](drm-flags.md) , ovvero un **valore DWORD** usato per specificare i diritti da applicare a una licenza di DRM versione 1 locale durante la copia del contenuto da un CD.</span><span class="sxs-lookup"><span data-stu-id="47998-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="47998-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47998-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47998-115">**Lettura di file protetti**</span><span class="sxs-lookup"><span data-stu-id="47998-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




