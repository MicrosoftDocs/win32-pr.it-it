---
title: Proprietà AudioQualityMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato. Per impostazione predefinita, questo valore è impostato su 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioQualityMode
- Servizi Desktop remoto proprietà AudioQualityMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AudioQualityMode
- Servizi Desktop remoto proprietà AudioQualityMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301892"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>Proprietà IMsRdpClientAdvancedSettings7:: AudioQualityMode

Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato. Per impostazione predefinita, questo valore è impostato su 0.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Valore proprietà

Valore che specifica la modalità di qualità audio.

I valori possibili sono:

<dt>

0
</dt> <dd>

Qualità audio dinamica. Questa è l'impostazione predefinita per la qualità audio. Il server regola dinamicamente la qualità dell'output audio in risposta alle condizioni della rete e alle funzionalità client e server.

</dd> <dt>

1
</dt> <dd>

Qualità audio media. Il server utilizza un formato fisso ma compresso per l'output audio.

</dd> <dt>

2
</dt> <dd>

Qualità audio elevata. Il server fornisce l'output audio in formato PCM non compresso con un sovraccarico di elaborazione inferiore per la latenza.

</dd> </dl>

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

 

 





