---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina se un tipo di notifica specificato è supportato dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0c5097f89583f0f6b04e0e8fb033446aae45743a8fb5a7fe9134f34bcc5e05fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118705"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>Metodo IDXCoreAdapterFactory::IsNotificationTypeSupported

Determina se un tipo di notifica specificato è supportato dal sistema operativo. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo di notifica per cui si esegue una query sul supporto. Per informazioni sui tipi di notifica, vedere la tabella in [DXCoreNotificationType.](./ne-dxcore_interface-dxcorenotificationtype.md)

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce `true` se il tipo di notifica è supportato dal sistema. In caso contrario, restituisce `false`.

## <a name="remarks"></a>Commenti

È possibile chiamare **IsNotificationTypeSupported** per determinare se un determinato tipo di notifica è noto a questa versione del sistema operativo. Ad esempio, un tipo di notifica introdotto in una particolare versione di Windows è sconosciuto alle versioni precedenti di Windows.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [Riferimenti DXCore,](../dxcore-reference.md)GUID degli attributi dell'adapter [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)