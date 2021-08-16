---
description: Il tipo di enumerazione WPD PARAMETER USAGE TYPES descrive come viene usato un parametro di metodo \_ \_ in un determinato \_ metodo.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 8ece49d1b961ce6ce5c14241d14bf69480e1eb79028f57a2cb959f5d7c4b79dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842068"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>Enumerazione WPD \_ PARAMETER \_ USAGE \_ TYPES

Il [**tipo di enumerazione WPD PARAMETER USAGE \_ \_ \_ TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descrive come viene usato un parametro di metodo in un determinato metodo.

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

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**RESTITUZIONE DELL'UTILIZZO \_ DEI \_ PARAMETRI WPD \_**
</dt> <dd>

Il parametro riceve il valore restituito, se specificato dal metodo .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**UTILIZZO DEI PARAMETRI WPD \_ \_ \_ IN**
</dt> <dd>

Il parametro contiene un valore di input prima che venga chiamato il metodo .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**UTILIZZO DEI PARAMETRI WPD \_ \_ \_ OUT**
</dt> <dd>

Il parametro contiene un valore di output quando il metodo restituisce .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**INOUT UTILIZZO \_ \_ DEI PARAMETRI WPD \_**
</dt> <dd>

Il parametro contiene un valore di input prima che venga chiamato il metodo e un valore di output quando viene restituito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

