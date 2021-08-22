---
description: Recupera le impostazioni di contesto predefinite per il tablet.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: Metodo ITablet::GetDefaultContextSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 646756a924bd9b848f2141b796205f2cf2374140811b7dd87f8ffd64c69ee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336261"
---
# <a name="itabletgetdefaultcontextsettings-method"></a>Metodo ITablet::GetDefaultContextSettings

Recupera le impostazioni di contesto predefinite per il tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTCS* \[ Cambio\]
</dt> <dd>

Impostazioni di contesto predefinite per il tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

