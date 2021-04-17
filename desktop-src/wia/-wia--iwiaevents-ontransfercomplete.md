---
description: Evento che si verifica quando un trasferimento dei dati viene completato correttamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231563"
---
# <a name="wiaontransfercomplete-event"></a>Evento WIA. OnTransferComplete

Evento che si verifica quando un trasferimento dei dati viene completato correttamente.

## <a name="syntax"></a>Sintassi


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Item* 
</dt> <dd>

Oggetto [**elemento**](-wia-item.md) trasferito.

</dd> <dt>

*Percorso* 
</dt> <dd>

Il percorso e il nome file dell'immagine trasferita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

WIA notifica allo script o all'applicazione quando un trasferimento dati, un'immagine o un suono viene completato correttamente. Implementare la subroutine **objWia** \_ **OnTransferComplete ()** per consentire all'applicazione o allo script di rispondere al completamento del trasferimento dei dati.

Ad esempio, potrebbe essere necessario che uno script visualizzi un'immagine dopo che è stata trasferita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




