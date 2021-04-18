---
description: Inizializza la \_ libreria aux klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Funzione AuxKlibInitialize (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331973"
---
# <a name="auxklibinitialize-function"></a>AuxKlibInitialize (funzione)

Inizializza la \_ libreria aux klib. Questa funzione deve essere chiamata prima che sia possibile chiamare qualsiasi altra funzione nella libreria.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in ntstatus. h, disponibile in WDK.

## <a name="remarks"></a>Commenti

La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|------------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Libreria API ausiliaria Windows versione 1,0 o successiva<br/>                            |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl>   |
| Libreria<br/>         | <dl> <dt>Aux \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




