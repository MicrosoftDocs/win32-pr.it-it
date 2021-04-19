---
title: Metodo ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardColors Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardColors
- Framework dei servizi di testo del metodo GetSoftKeyboardColors, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "106320171"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>Metodo ISoftKbd:: GetSoftKeyboardColors

Il metodo **ISoftKbd:: GetSoftKeyboardColors** Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ColorType* \[ in\]
</dt> <dd>

Valore che specifica il tipo di colore da recuperare per la tastiera soft. I valori possibili sono definiti per l'enumerazione [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*lpColor* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera un valore [**COLORREF**](/windows/desktop/gdi/colorref) a 32 bit specificando un colore RGB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno dei parametri non è valido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardColors**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

