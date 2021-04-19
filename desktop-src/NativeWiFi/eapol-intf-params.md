---
description: Contiene i parametri di configurazione avvio EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Struttura EAPOL_INTF_PARAMS (wzcsapi. h)
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
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313762"
---
# <a name="eapol_intf_params-structure"></a>\_Struttura avvio EAPOL INTF \_ params

\[**Avvio EAPOL \_ INTF \_ params** non è più supportato a partire da Windows Vista e windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

Contiene i parametri di configurazione avvio EAPOL.

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

Tipo di estensione EAP da usare. Impostare su 0x00000013 per EAP-TLS e 0x00000026 per PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Dimensioni dell'identificatore di rete.

</dd> <dt>

**bSSID**
</dt> <dd>

Identificatore di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il file di intestazione wzcsapi. h non è disponibile nel Windows SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                       |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




