---
title: Proprietà BasicDevice. icons
description: Ottiene un vettore di interfacce IDeviceIcon.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- API di streaming multimediale delle proprietà delle icone
- API di streaming multimediale proprietà icone, interfaccia BasicDevice
- API di streaming multimediale dell'interfaccia BasicDevice, proprietà icons
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398996"
---
# <a name="basicdeviceicons-property"></a>Proprietà BasicDevice. icons

Ottiene un vettore di interfacce [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>Valore proprietà

Raccolta enumerabile di puntatori dell'interfaccia [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 