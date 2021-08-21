---
title: Metodo ISoftKbd GetSoftKeyboardTextFont (Softkbdc.h)
description: Il metodo ISoftKbd GetSoftKeyboardTextFont recupera il tipo di carattere del testo usato da una tastiera soft.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Metodo GetSoftKeyboardTextFont Framework servizi di testo
- Metodo GetSoftKeyboardTextFont Framework servizi di testo interfaccia , ISoftKbd
- Interfaccia ISoftKbd Framework servizi di testo, metodo GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d1dcd1d069339c9bfb703bc37cda7e5972fceb707924cdabb868081ea308c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877755"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>Metodo ISoftKbd::GetSoftKeyboardTextFont

Il **metodo ISoftKbd::GetSoftKeyboardTextFont** recupera il tipo di carattere del testo usato da una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLogFont* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera una [**struttura LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che definisce il tipo di carattere del testo per la tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro pLogFont* non è valido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

