---
title: Specifica delle azioni da eseguire
description: Specifica delle azioni da eseguire
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF), specifica delle azioni
- ASF (Advanced Systems Format), specifica delle azioni
- DRM (Digital Rights Management), specifica delle azioni
- DRM (Digital Rights Management),specifica delle azioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d27df2904aee061deb252e08b59e1e88e4d1cd9e151290cd940fc48a650404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807801"
---
# <a name="specifying-the-actions-to-be-performed"></a>Specifica delle azioni da eseguire

Quando si chiama [**WMCreateReader per la**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) prima volta per creare l'oggetto reader, il secondo parametro è **un'operazione OR** bit per bit di valori RIGHTS [**WMT. \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) Usare questo parametro per specificare quali azioni verranno accettate dall'applicazione per il primo file da aprire. Queste azioni corrispondono direttamente ai diritti che possono essere specificati nella licenza. Nelle chiamate successive a [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)è possibile modificare i diritti necessari chiamando [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specificando la costante definita per la proprietà [**DRM \_ Rights**](drm-rights.md) e usando valori letterali stringa (di tipo **WCHAR)** separati da punti e virgola per identificare i diritti. Il frammento di codice seguente richiede quattro diritti: riprodurre il file, copiarlo in un dispositivo e riprodurlo come parte di una playlist collaborativa.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Non confondere la proprietà [**DRM \_ Rights**](drm-rights.md) con la proprietà [**DRM \_ Flags,**](drm-flags.md) che è un **valore DWORD** usato per specificare i diritti da applicare a una licenza DRM locale versione 1 durante la copia di contenuto da un CD.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




