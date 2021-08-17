---
description: Converte una stringa di caratteri Unicode o un singolo carattere in minuscolo.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Funzione CharLowerWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9a02e89713dd82de63817c00d5402fabe991fed565ebe33fa40286ad30058d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710751"
---
# <a name="charlowerwrapw-function"></a>Funzione CharLowerWrapW

\[**CharLowerWrapW** è disponibile per l'uso in Windows XP. Potrebbe non essere disponibile nelle versioni successive. È consigliabile [**usare CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) al suo posto.\]

Converte una stringa di caratteri Unicode o un singolo carattere in minuscolo. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto.

> [!Note]  
> **CharLowerWrapW** è un wrapper per la **funzione CharLowerW.** Per altre note sull'utilizzo, vedere la pagina [**CharLower.**](/windows/win32/api/winuser/nf-winuser-charlowera)

 

## <a name="syntax"></a>Sintassi


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pch* \[ in, out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a una stringa Unicode con terminazione Null o a un singolo carattere. Se la parola più importante di questo parametro è zero, la parola di ordine più basso deve contenere un solo carattere da convertire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LPWSTR**

Se *pch* è una stringa di caratteri, la funzione restituisce un puntatore alla stringa convertita. Poiché la stringa viene convertita sul posto, il valore restituito è uguale a *pch*.

Se *pch* è un singolo carattere, il valore restituito è un valore a 32 bit la cui parola più alta è zero e la parola meno importante contiene il carattere convertito.

Non è presente alcuna indicazione di esito positivo o negativo. L'errore è raro. Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Il metodo preferito è usare [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) insieme a Microsoft Layer for Unicode (MSLU).

**CharLowerWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 38.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
