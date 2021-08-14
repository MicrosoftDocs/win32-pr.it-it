---
description: Determina se un carattere è alfabetico o numerico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Funzione IsCharAlphaNumericWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452996"
---
# <a name="ischaralphanumericwrapw-function"></a>Funzione IsCharAlphaNumericWrapW

\[**IsCharAlphaNumericWrapW** è disponibile per l'uso in Windows XP. Non sarà disponibile nelle versioni successive. È consigliabile [**usare IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) al suo posto.\]

Determina se un carattere è alfabetico o numerico. Questa determinazione si basa sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite Pannello di controllo.

> [!Note]  
> **IsCharAlphaNumericWrapW** è un wrapper per la **funzione IsCharAlphaNumericW.** Per altre note sull'utilizzo, vedere la pagina [**IsCharAlphaNumeric.**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)

 

## <a name="syntax"></a>Sintassi


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ch* \[ Pollici\]
</dt> <dd>

Tipo: **WCHAR**

Carattere Unicode da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Se il carattere è alfanumerico, il valore restituito è diverso da zero.

Se il carattere non è alfanumerico, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**IsCharAlphaNumericWrapW** offre la possibilità di usare stringhe Unicode nei sistemi operativi precedenti Windows XP. Il metodo preferito è usare [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) insieme al livello Microsoft per Unicode (MSLU).

**IsCharAlphaNumericWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 28.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
