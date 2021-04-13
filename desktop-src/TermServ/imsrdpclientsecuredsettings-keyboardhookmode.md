---
title: Proprietà KeyboardHookMode di IMsRdpClientSecuredSettings
description: Specifica le impostazioni di Reindirizzamento da tastiera, che specificano come e quando applicare il tasto di scelta rapida di Windows, ad esempio ALT + TAB.
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà KeyboardHookMode
- Servizi Desktop remoto proprietà KeyboardHookMode, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà KeyboardHookMode
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
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400442"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>Proprietà IMsRdpClientSecuredSettings:: KeyboardHookMode

Specifica le impostazioni di Reindirizzamento da tastiera, che specificano come e quando applicare il tasto di scelta rapida di Windows, ad esempio ALT + TAB.

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

Applicare le combinazioni di tasti solo localmente nel computer client.

</dd> <dt>

1
</dt> <dd>

Applicare le combinazioni di tasti al server remoto.

</dd> <dt>

2
</dt> <dd>

Applicare le combinazioni di tasti al server remoto solo quando il client è in esecuzione in modalità schermo intero. Si tratta del valore predefinito.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Non è possibile impostare queste proprietà quando il controllo è connesso.

Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                       |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





