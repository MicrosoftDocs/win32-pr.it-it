---
title: Proprietà Enabled di IRemoteDesktopClientTouchPointer
description: Indica se la funzionalità del puntatore a tocco è abilitata nel controllo client del contenitore di app RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà abilitata
- Servizi Desktop remoto proprietà Enabled, interfaccia IRemoteDesktopClientTouchPointer
- Interfaccia IRemoteDesktopClientTouchPointer Servizi Desktop remoto, proprietà Enabled
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
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301982"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Proprietà IRemoteDesktopClientTouchPointer:: Enabled

Indica se la funzionalità del puntatore a tocco è abilitata nel controllo client del contenitore di app RDP.

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

**true** se la funzionalità del puntatore a tocco è abilitata; in caso contrario, **false**.

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

 

