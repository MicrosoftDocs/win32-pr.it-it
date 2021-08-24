---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Funzione di callback (implementata dall'applicazione), chiamata da un oggetto DXCore per gli eventi di notifica.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787101"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK callback

Funzione di callback (implementata dall'applicazione), chiamata da un oggetto DXCore per gli eventi di notifica.

## <a name="syntax"></a>Sintassi

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Parametri

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo di notifica che rappresenta questa chiamata. Vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) per informazioni sui tipi validi con quali tipi di oggetti.

### <a name="object"></a>object

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Oggetto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) che genera la notifica.

### <a name="context-in"></a>context [in]

Tipo: **\* void**

Puntatore, che può essere , a `nullptr` un oggetto contenente informazioni di contesto.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)