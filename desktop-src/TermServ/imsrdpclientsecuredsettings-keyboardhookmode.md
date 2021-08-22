---
title: Proprietà KeyboardHookMode IMsRdpClientSecuredSettings
description: Specifica le impostazioni di reindirizzamento della tastiera, che specificano come e quando applicare Windows scelta rapida da tastiera ,ad esempio ALT+TAB.
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Proprietà KeyboardHookMode Servizi Desktop remoto
- Proprietà KeyboardHookMode Servizi Desktop remoto, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto , proprietà KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657591"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>Proprietà IMsRdpClientSecuredSettings::KeyboardHookMode

Specifica le impostazioni di reindirizzamento della tastiera, che specificano come e quando applicare Windows scelta rapida da tastiera ,ad esempio ALT+TAB.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Valore proprietà

Nuove impostazioni. Questo parametro può avere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Applicare combinazioni di tasti solo localmente nel computer client.

</dd> <dt>

1
</dt> <dd>

Applicare combinazioni di tasti nel server remoto.

</dd> <dt>

2
</dt> <dd>

Applicare combinazioni di tasti al server remoto solo quando il client è in esecuzione in modalità schermo intero. Si tratta del valore predefinito.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Queste proprietà non possono essere impostate quando il controllo è connesso.

Per altre [informazioni, vedere Fornire la sicurezza client RDP.](providing-for-rdp-client-security.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                       |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





