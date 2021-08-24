---
description: Inizializza la libreria Aux \_ klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Funzione AuxKlibInitialize (Aux \_ klib.h)
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
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654881"
---
# <a name="auxklibinitialize-function"></a>Funzione AuxKlibInitialize

Inizializza la libreria Aux \_ klib. Questa funzione deve essere chiamata prima di poter chiamare qualsiasi altra funzione nella libreria.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in Ntstatus.h, disponibile in WDK.

## <a name="remarks"></a>Commenti

La libreria di oggetti che implementa questa API può essere scaricata da [qui.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|------------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria API ausiliaria versione 1.0 o successiva<br/>                            |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl>   |
| Libreria<br/>         | <dl> <dt>Aux \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




