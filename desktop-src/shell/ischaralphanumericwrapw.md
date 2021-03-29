---
description: Determina se un carattere è un carattere alfabetico o numerico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW (funzione)
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
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978122"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW (funzione)

\[**IsCharAlphaNumericWrapW** è disponibile per l'utilizzo in Windows XP. Non sarà disponibile nelle versioni successive. È consigliabile usare [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) al suo posto.\]

Determina se un carattere è un carattere alfabetico o numerico. Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.

> [!Note]  
> **IsCharAlphaNumericWrapW** è un wrapper per la funzione **IsCharAlphaNumericW** . Per ulteriori note sull'utilizzo, vedere la pagina [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .

 

## <a name="syntax"></a>Sintassi


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ch* \[ in\]
</dt> <dd>

Tipo: **WCHAR**

Carattere Unicode da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Se il carattere è alfanumerico, il valore restituito è diverso da zero.

Se il carattere non è alfanumerico, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**IsCharAlphaNumericWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP. Il metodo preferito consiste nell'usare [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) insieme a Microsoft Layer for Unicode (MSLU).

**IsCharAlphaNumericWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 28.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
