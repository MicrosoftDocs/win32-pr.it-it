---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina se un tipo di notifica specificato è supportato dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338583"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>Metodo IDXCoreAdapterFactory:: IsNotificationTypeSupported

Determina se un tipo di notifica specificato è supportato dal sistema operativo. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo di notifica di cui si sta eseguendo una query sul supporto per. Per informazioni sui tipi di notifica, vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se il tipo di notifica è supportato dal sistema. In caso contrario, restituisce  `false` .

## <a name="remarks"></a>Commenti

È possibile chiamare **IsNotificationTypeSupported** per determinare se un tipo di notifica specificato è noto a questa versione del sistema operativo. Ad esempio, un tipo di notifica introdotto in una particolare versione di Windows è sconosciuto alle versioni precedenti di Windows.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)