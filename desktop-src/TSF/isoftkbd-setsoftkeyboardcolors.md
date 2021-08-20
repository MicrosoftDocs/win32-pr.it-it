---
title: Metodo ISoftKbd SetSoftKeyboardColors (Softkbdc.h)
description: Il metodo ISoftKbd SetSoftKeyboardColors imposta il colore della tastiera soft per il tipo di colore specificato.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Metodo SetSoftKeyboardColors Framework servizi di testo
- Metodo SetSoftKeyboardColors Framework servizi di testo, interfaccia ISoftKbd
- Interfaccia ISoftKbd Framework servizi di testo metodo SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877372"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>Metodo ISoftKbd::SetSoftKeyboardColors

Il **metodo ISoftKbd::SetSoftKeyboardColors** imposta il colore della tastiera soft per il tipo di colore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*colorType* \[ Pollici\]
</dt> <dd>

Valore che specifica il tipo di colore per la tastiera soft. I valori possibili sono definiti per [**l'enumerazione COLORTYPE.**](/windows/win32/api/icm/ne-icm-colortype)

</dd> <dt>

*Colore* \[ Pollici\]
</dt> <dd>

Valore [**COLORREF**](/windows/desktop/gdi/colorref) a 32 bit che specifica un colore RGB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno dei parametri non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

