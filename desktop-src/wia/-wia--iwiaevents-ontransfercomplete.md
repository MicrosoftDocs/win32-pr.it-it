---
description: Evento che si verifica quando un trasferimento dei dati viene completato correttamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento Wia.OnTransferComplete
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
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209275"
---
# <a name="wiaontransfercomplete-event"></a>Evento Wia.OnTransferComplete

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

Oggetto [**Item**](-wia-item.md) trasferito.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso e nome file dell'immagine trasferita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

WIA invia una notifica allo script o all'applicazione quando un trasferimento dei dati, un'immagine o un suono viene completato correttamente. Implementare **la subroutine objWia** \_ **OnTransferComplete()** per consentire allo script o all'applicazione di rispondere al completamento del trasferimento dei dati.

Ad esempio, potrebbe essere necessario che uno script visualizza un'immagine dopo il trasferimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




