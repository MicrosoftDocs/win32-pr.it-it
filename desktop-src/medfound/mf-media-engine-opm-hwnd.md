---
description: Specifica una finestra per il motore multimediale per applicare le protezioni di output Protection Manager (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Attributo MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968881"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ \_ Attributo HWND hWnd del motore multimediale MF

Specifica una finestra per il motore multimediale per applicare le protezioni di [Output Protection Manager](output-protection-manager.md) (OPM).

## <a name="data-type"></a>Tipo di dati

**HWND** archiviato come **UInt64**

## <a name="remarks"></a>Commenti

Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.

Per abilitare le protezioni di OPM per la riproduzione video, l'applicazione deve eseguire una delle operazioni seguenti:

-   Impostare l'attributo HWND per la [ \_ \_ \_ riproduzione \_ del motore multimediale MF](mf-media-engine-playback-hwnd.md) quando si crea il motore multimediale.
-   Impostare l' \_ \_ attributo HWND hWnd del motore multimediale MF \_ quando si \_ Crea il motore multimediale.
-   Chiamare [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) in qualsiasi momento dopo aver creato il motore multimediale, ma prima di visualizzare il contenuto protetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore multimediale](media-engine-attributes.md)
</dt> </dl>

 

 




