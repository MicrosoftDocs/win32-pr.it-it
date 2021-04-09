---
title: DrawTextExPrivWrap (funzione)
description: Disegna il testo formattato nel rettangolo specificato. Questa funzione esegue il wrapping di una chiamata a DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Controlli Windows per la funzione DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964941"
---
# <a name="drawtextexprivwrap-function"></a>DrawTextExPrivWrap (funzione)

\[**DrawTextExPrivWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. Si consiglia invece di usare direttamente [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .\]

Disegna il testo formattato nel rettangolo specificato. Questa funzione esegue il wrapping di una chiamata a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="syntax"></a>Sintassi


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HDC* \[ in\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo in cui eseguire il progetto.

</dd> <dt>

*lpchText* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer contenente il testo da creare. Se il parametro *cchText* è-1, la stringa deve essere con terminazione null.

Se *dwDTFormat* include DT \_ MODIFYSTRING, la funzione potrebbe aggiungere fino a quattro caratteri aggiuntivi a questa stringa. Il buffer che contiene la stringa deve essere sufficientemente grande da contenere questi caratteri aggiuntivi.

</dd> <dt>

*cchText* \[ in\]
</dt> <dd>

Tipo: **int**

Lunghezza della stringa a cui punta *lpchText*. Se *cchText* è-1, si presuppone che il parametro *lpchText* sia un puntatore a una stringa con terminazione null e [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcoli automaticamente il numero di caratteri.

</dd> <dt>

*LPRC* \[ in uscita\]
</dt> <dd>

Tipo: **lpRect**

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.

</dd> <dt>

*dwDTFormat* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opzioni di formattazione. Per un elenco completo delle opzioni, vedere la documentazione relativa a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .

</dd> <dt>

*lpDTParams* \[ in\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntatore a una struttura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) che specifica le opzioni di formattazione aggiuntive. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche. Se si specifica **DT \_ vCenter** o **DT \_ Bottom** , il valore restituito è l'offset dal **primo** membro di *LPRC* alla fine del testo disegnato.

Se la funzione ha esito negativo, il valore restituito è zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**DrawTextExPrivWrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 416 da ComCtl32.dll per ottenere un puntatore a funzione.

Per ulteriori osservazioni, vedere [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 6,0 o successiva)</dt> </dl> |



 

