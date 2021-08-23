---
description: Contiene i parametri di configurazione EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 3359454196735b8100ea40a9b4add2e8e0398c336bf254eb507b0a4e63a86e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685241"
---
# <a name="eapol_intf_params-structure"></a>Struttura EAPOL \_ INTF \_ PARAMS

\[**EAPOL \_ INTF \_ PARAMS** non è più supportato a Windows Vista e Windows Server 2008. Usare invece [l'API Wi-Fi nativa](native-wifi-reference.md), che offre funzionalità simili. Per altre informazioni, vedere [Informazioni sull'API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

Contiene i parametri di configurazione EAPOL.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Versione del chiamante. Il valore predefinito è 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**dwEapFlags**
</dt> <dd>

Non usato.

</dd> <dt>

**dwEapType**
</dt> <dd>

Tipo di estensione EAP da utilizzare. Impostare su 0x00000013 per EAP-TLS e 0x00000026 per PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Dimensioni dell'identificatore di rete.

</dd> <dt>

**Bssid**
</dt> <dd>

Identificatore di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il file di intestazione wzcsapi.h non è disponibile in Windows SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                       |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



 

 




