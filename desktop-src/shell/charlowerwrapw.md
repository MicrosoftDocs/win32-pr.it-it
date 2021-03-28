---
description: Converte una stringa di caratteri Unicode o un singolo carattere in caratteri minuscoli.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW (funzione)
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
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525399"
---
# <a name="charlowerwrapw-function"></a>CharLowerWrapW (funzione)

\[**CharLowerWrapW** è disponibile per l'utilizzo in Windows XP. Potrebbe non essere disponibile nelle versioni successive. È consigliabile usare [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) al suo posto.\]

Converte una stringa di caratteri Unicode o un singolo carattere in caratteri minuscoli. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto.

> [!Note]  
> **CharLowerWrapW** è un wrapper per la funzione **CharLowerW** . Per ulteriori note sull'utilizzo, vedere la pagina [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) .

 

## <a name="syntax"></a>Sintassi


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PCH* \[ in uscita\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a una stringa Unicode con terminazione null o a un singolo carattere. Se la parola più significativa di questo parametro è zero, la parola di ordine inferiore deve contenere solo un singolo carattere da convertire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LPWSTR**

Se *PCH* è una stringa di caratteri, la funzione restituisce un puntatore alla stringa convertita. Poiché la stringa viene convertita sul posto, il valore restituito è uguale a *PCH*.

Se *PCH* è un singolo carattere, il valore restituito è un valore a 32 bit la cui parola più elevata è zero e la parola di ordine inferiore contiene il carattere convertito.

Non è presente alcuna indicazione di esito positivo o negativo. L'errore è raro. Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Il metodo preferito consiste nell'usare [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) insieme a Microsoft Layer for Unicode (MSLU).

**CharLowerWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 38.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
