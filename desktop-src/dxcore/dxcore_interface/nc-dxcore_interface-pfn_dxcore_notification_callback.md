---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Funzione di callback, implementata dall'applicazione, che viene chiamata da un oggetto DXCore per gli eventi di notifica.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963335"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>CALLBACK PFN_DXCORE_NOTIFICATION_CALLBACK

Funzione di callback, implementata dall'applicazione, che viene chiamata da un oggetto DXCore per gli eventi di notifica.

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

Tipo di notifica che rappresenta questa chiamata. Per informazioni sui tipi validi con i tipi di oggetti, vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="object"></a>object

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Oggetto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) che genera la notifica.

### <a name="context-in"></a>Context [in]

Tipo: **void \***

Puntatore, che può essere `nullptr` , a un oggetto che contiene informazioni sul contesto.

## <a name="see-also"></a>Vedi anche

Guida di riferimento a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)