---
title: Metodo ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardTextFont imposta il tipo di carattere del testo utilizzato da una tastiera soft.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardTextFont
- Framework dei servizi di testo del metodo SetSoftKeyboardTextFont, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302180"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>Metodo ISoftKbd:: SetSoftKeyboardTextFont

Il metodo **ISoftKbd:: SetSoftKeyboardTextFont** imposta il tipo di carattere del testo utilizzato da una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLogFont* \[ in\]
</dt> <dd>

Puntatore a una struttura [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che definisce il tipo di carattere del testo per la tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *pLogFont* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

