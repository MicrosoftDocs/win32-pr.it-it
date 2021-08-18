---
title: Interfaccia IMsRdpInputSink
description: Sink di input del desktop remoto.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpInputSink Servizi Desktop remoto
- Interfaccia IMsRdpInputSink Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2167106577a005f6e4ba13ee77edcdbc77302efad9de00395fc7360ade4c5720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058844"
---
# <a name="imsrdpinputsink-interface"></a>Interfaccia IMsRdpInputSink

Sink di input del desktop remoto.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpInputSink** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpInputSink** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpInputSink** include questi metodi.



| Metodo                                                               | Descrizione                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Aggiunge l'input tocco.<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Iniziare il touch frame.<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Frame tocco finale.<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Invia l'evento della tastiera.<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Invia l'evento del pulsante del mouse.<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Invia l'evento di spostamento del mouse.<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Invia l'evento della rotellina del mouse.<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Invia l'evento di sincronizzazione.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                 |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                      |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink è definito come 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

