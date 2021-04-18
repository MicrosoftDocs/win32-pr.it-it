---
description: Il \_ tipo di enumerazione WPD Focus Modes \_ descrive la modalità messa a fuoco usata da un dispositivo di acquisizione di immagini ancora.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumerazione WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328964"
---
# <a name="wpd_focus_modes-enumeration"></a>\_Enumerazione WPD Focus \_ modes

Il tipo di enumerazione **WPD \_ Focus \_** Modes descrive la modalità messa a fuoco usata da un dispositivo di acquisizione di immagini ancora.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**lo \_ stato attivo WPD non è \_ definito**
</dt> <dd>

La modalità messa a fuoco non è stata specificata.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**Manuale di WPD \_ Focus \_**
</dt> <dd>

Specifica lo stato attivo manuale.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD \_ messa a fuoco \_ automatica**
</dt> <dd>

Specifica lo stato attivo automatico, controllato dal dispositivo.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_macro messa a fuoco \_ automatica WPD \_**
</dt> <dd>

Specifica che il dispositivo deve passare automaticamente tra la macro e lo stato attivo normale, a seconda delle esigenze.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Focus \_ mode](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




