---
title: GetTextExtentPoint32Wrap (funzione)
description: Calcola la larghezza e l'altezza della stringa di testo specificata. Questa funzione esegue il wrapping di una chiamata a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Controlli Windows per la funzione GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740111"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap (funzione)

\[**GetTextExtentPoint32Wrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. Si consiglia invece di usare direttamente [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) .\]

Calcola la larghezza e l'altezza della stringa di testo specificata. Questa funzione esegue il wrapping di una chiamata a [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="syntax"></a>Sintassi


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HDC* \[ in\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo.

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer contenente il testo da disegnare. La stringa non deve essere con terminazione zero, poiché *cbCount* specifica la lunghezza della stringa.

</dd> <dt>

*cbCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza, in byte, della stringa a cui punta *lpString*.

</dd> <dt>

*lpSize* \[ out\]
</dt> <dd>

Tipo: **LPSIZE**

Quando termina, questo metodo contiene un puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che contiene le dimensioni della stringa, in unità logiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Restituisce un valore diverso da zero se ha esito positivo; in caso contrario, 0.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**GetTextExtentPoint32Wrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 420 da ComCtl32.dll per ottenere un puntatore a funzione.

Per ulteriori osservazioni, vedere [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5,81 o successiva)</dt> </dl> |



 

