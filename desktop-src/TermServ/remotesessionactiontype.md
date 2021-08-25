---
title: Enumerazione RemoteSessionActionType
description: Consente di specificare il tipo di azione remota.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Enumerazione RemoteSessionActionType Servizi Desktop remoto
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107ee44f058d776a906fef37b2e384ed6d8970224c44a6846b257c5f336c515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865711"
---
# <a name="remotesessionactiontype-enumeration"></a>Enumerazione RemoteSessionActionType

Consente di specificare il tipo di azione remota.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**
</dt> <dd>

Visualizza gli accessi nella sessione remota.

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**
</dt> <dd>

Visualizza la barra dell'app nella sessione remota.

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**
</dt> <dd>

Ancora l'applicazione nella sessione remota. Questa opzione è stata deprecata e non deve essere usata.

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**
</dt> <dd>

Determina la visualizzazione della schermata iniziale nella sessione remota.

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**
</dt> <dd>

Fa sì che la finestra del commutatore dell'applicazione sia visualizzata nella sessione remota. Questo è lo stesso dell'utente che preme ALT+TAB.

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**
</dt> <dd>

Determina la visualizzazione del Centro notifiche nella sessione remota. Questo è lo stesso dell'utente che preme Win+A.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 e Windows 8:** Questo valore non è supportato prima di Windows Server 2016 e Windows 10.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient8::SendRemoteAction**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





