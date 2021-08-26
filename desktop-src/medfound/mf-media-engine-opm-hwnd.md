---
description: Specifica una finestra per il motore multimediale per applicare le protezioni OPM (Output Protection Manager).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND attributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1079e7b9503c73ea678e4f9fd3642ec94fe43a1326e6f33a635f81d1bc1a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013071"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>Attributo MF \_ MEDIA \_ ENGINE \_ OPM \_ HWND

Specifica una finestra in cui il motore multimediale applica le protezioni [OPM (Output Protection Manager).](output-protection-manager.md)

## <a name="data-type"></a>Tipo di dati

**HWND archiviato** come **UINT64**

## <a name="remarks"></a>Commenti

Questo attributo viene usato con il [**metodo IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.

Per abilitare le protezioni OPM per la riproduzione video, l'applicazione deve eseguire una delle operazioni seguenti:

-   Impostare [l'attributo \_ \_ \_ \_ HWND MF MEDIA ENGINE PLAYBACK durante](mf-media-engine-playback-hwnd.md) la creazione del motore multimediale.
-   Impostare l'attributo \_ \_ HWND MF MEDIA ENGINE \_ \_ OPM durante la creazione del motore multimediale.
-   Chiamare [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) in qualsiasi momento dopo la creazione del motore multimediale, ma prima che venga visualizzato il contenuto protetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore multimediale](media-engine-attributes.md)
</dt> </dl>

 

 




