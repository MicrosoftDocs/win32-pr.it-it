---
title: Enumerazione RemoteWindowDisplayedAttribute
description: Utilizzato con il metodo per specificare le informazioni sull'evento.
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione RemoteWindowDisplayedAttribute
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301976"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a>Enumerazione RemoteWindowDisplayedAttribute

Utilizzato con il metodo per specificare le informazioni sull'evento.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**
</dt> <dd></dd> <dt>

<span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**
</dt> <dd></dd> <dt>

<span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





