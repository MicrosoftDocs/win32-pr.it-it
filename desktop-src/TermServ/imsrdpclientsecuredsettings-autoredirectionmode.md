---
title: Proprietà AudioRedirectionMode di IMsRdpClientSecuredSettings
description: Specifica le impostazioni di reindirizzamento audio, che specificano se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519229"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>Proprietà IMsRdpClientSecuredSettings:: AudioRedirectionMode

Specifica le impostazioni di reindirizzamento audio, che specificano se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Valore proprietà

Nuove impostazioni. Questo parametro può avere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Reindirizza i suoni al client. Rappresenta il valore predefinito.

</dd> <dt>

1
</dt> <dd>

Riprodurre suoni nel computer remoto.

</dd> <dt>

2
</dt> <dd>

Disabilitare il reindirizzamento del suono; non riprodurre suoni sul server.

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

 

 





