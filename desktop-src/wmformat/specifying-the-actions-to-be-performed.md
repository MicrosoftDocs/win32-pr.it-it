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
# <a name="specifying-the-actions-to-be-performed"></a>Specifica delle azioni da eseguire

Quando si chiama prima [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) per creare l'oggetto Reader, il secondo parametro è **un operatore OR** bit per bit di valori di [**\_ diritti WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) . Utilizzare questo parametro per specificare le azioni che verranno intraprese dall'applicazione sul primo file da aprire. Queste azioni corrispondono direttamente ai diritti che è possibile specificare nella licenza. Nelle chiamate successive a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)è possibile modificare i diritti richiesti chiamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specificando la costante definita per la proprietà [**\_ Rights DRM**](drm-rights.md) e usando i valori letterali stringa (di tipo **WCHAR**) separati da punto e virgola per identificare i diritti. Il frammento di codice seguente richiede quattro diritti: riprodurre il file, copiarlo in un dispositivo e riprodurlo come parte di una playlist collaborativa.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Non confondere la [**proprietà \_ dei diritti DRM**](drm-rights.md) con la proprietà dei [**\_ flag DRM**](drm-flags.md) , ovvero un **valore DWORD** usato per specificare i diritti da applicare a una licenza di DRM versione 1 locale durante la copia del contenuto da un CD.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




