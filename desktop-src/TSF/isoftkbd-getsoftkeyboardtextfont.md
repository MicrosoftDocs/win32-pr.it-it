---
title: Metodo ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardTextFont Recupera il tipo di carattere del testo utilizzato da una tastiera soft.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardTextFont
- Framework dei servizi di testo del metodo GetSoftKeyboardTextFont, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardTextFont
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
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120818"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>Metodo ISoftKbd:: GetSoftKeyboardTextFont

Il metodo **ISoftKbd:: GetSoftKeyboardTextFont** Recupera il tipo di carattere del testo utilizzato da una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLogFont* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera una struttura [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che definisce il tipo di carattere del testo per la tastiera soft.

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

