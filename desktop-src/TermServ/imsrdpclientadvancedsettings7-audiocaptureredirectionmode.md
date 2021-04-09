---
title: Proprietà AudioCaptureRedirectionMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore booleano che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AudioCaptureRedirectionMode
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964426"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a>Proprietà IMsRdpClientAdvancedSettings7:: AudioCaptureRedirectionMode

Specifica o recupera un valore booleano che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a>Valore proprietà

Valore **\_ bool Variant** che specifica se l'acquisizione audio viene reindirizzata. Specificare **Variant \_ true** se si vuole che l'acquisizione audio venga reindirizzata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





