---
description: L'interfaccia IKeyFrameControl viene implementata da H. 323 MSP ed è disponibile solo negli oggetti flusso H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interfaccia IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329328"
---
# <a name="ikeyframecontrol-interface"></a>Interfaccia IKeyFrameControl

\[**IKeyFrameControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IKeyFrameControl** viene implementata da [h. 323 msp](h323-msp.md) ed è disponibile solo negli oggetti flusso h. 323. Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP. Dispone di due metodi che consentono all'applicazione di richiedere all'endpoint remoto di aggiornare l'immagine video con un fotogramma chiave.

## <a name="members"></a>Membri

L'interfaccia **IKeyFrameControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IKeyFrameControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IKeyFrameControl** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**PeriodicUpdatePicture**](ikeyframecontrol-periodicupdatepicture.md) | Configura un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini.<br/> |
| [**UpdatePicture**](ikeyframecontrol-updatepicture.md)                 | Chiede al mittente del video di aggiornare l'immagine.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

