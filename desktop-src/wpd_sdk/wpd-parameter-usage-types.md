---
description: Il \_ \_ \_ tipo di enumerazione dei tipi di utilizzo del parametro WPD descrive la modalità di utilizzo di un parametro di metodo in un determinato metodo.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumerazione WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326953"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>Enumerazione per i tipi di utilizzo del \_ parametro WPD \_ \_

Il tipo di enumerazione dei [**\_ tipi di \_ utilizzo \_ del parametro WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descrive la modalità di utilizzo di un parametro di metodo in un determinato metodo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_restituzione \_ utilizzo parametri WPD \_**
</dt> <dd>

Il parametro riceve il valore restituito, se specificato dal metodo.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_utilizzo parametri \_ WPD \_ in**
</dt> <dd>

Il parametro contiene un valore di input prima della chiamata al metodo.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_utilizzo parametri \_ WPD \_**
</dt> <dd>

Il parametro contiene un valore di output quando il metodo restituisce.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_utilizzo del parametro WPD \_ \_ InOut**
</dt> <dd>

Il parametro contiene un valore di input prima che venga chiamato il metodo e un valore di output quando viene restituito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

