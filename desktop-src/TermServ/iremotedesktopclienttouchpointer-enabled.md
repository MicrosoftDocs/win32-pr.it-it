---
title: Proprietà IRemoteDesktopClientTouchPointer Enabled
description: Indica se la funzionalità del puntatore tocco è abilitata nel controllo client del contenitore di app RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Impostazione delle proprietà abilitata Servizi Desktop remoto
- Proprietà abilitata Servizi Desktop remoto, interfaccia IRemoteDesktopClientTouchPointer
- Interfaccia IRemoteDesktopClientTouchPointer Servizi Desktop remoto proprietà Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ce04e38b41fce462973606f40f0099f010e6f4ab785900039e6771b0a9aaf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124851"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Proprietà IRemoteDesktopClientTouchPointer::Enabled

Indica se la funzionalità del puntatore tocco è abilitata nel controllo client del contenitore di app RDP.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valore proprietà

**true se** la funzionalità del puntatore tocco è abilitata; in caso contrario, **false.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                      |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ IRemoteDesktopClientTouchPointer è definito come 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

