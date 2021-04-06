---
title: DrawTextWrap (funzione)
description: Disegna il testo formattato nel rettangolo specificato. Formatta il testo in base al metodo specificato (espandendo le schede, giustificando i caratteri, suddividendo le righe e così via). Questa funzione esegue il wrapping di una chiamata a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Controlli Windows per la funzione DrawTextWrap
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963811"
---
# <a name="drawtextwrap-function"></a>DrawTextWrap (funzione)

\[**DrawTextWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. Si consiglia invece di utilizzare direttamente [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .\]

Disegna il testo formattato nel rettangolo specificato. Formatta il testo in base al metodo specificato (espandendo le schede, giustificando i caratteri, suddividendo le righe e così via). Questa funzione esegue il wrapping di una chiamata a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="syntax"></a>Sintassi


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HDC* \[ in\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo.

</dd> <dt>

*lpString* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer contenente il testo da creare. Se il parametro *nCount* è-1, la stringa deve essere con terminazione null.

Se *UFormat* include DT \_ MODIFYSTRING, la funzione potrebbe aggiungere fino a quattro caratteri aggiuntivi a questa stringa. Il buffer che contiene la stringa deve essere sufficientemente grande da contenere questi caratteri aggiuntivi.

</dd> <dt>

*nCount* \[ in\]
</dt> <dd>

Tipo: **int**

Lunghezza della stringa a cui punta *lpString*. Se *nCount* è-1, viene utilizzato il parametro *lpString* come puntatore a una stringa con terminazione null e [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcola automaticamente il numero di caratteri.

</dd> <dt>

*lpRect* \[ in uscita\]
</dt> <dd>

Tipo: **lpRect**

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.

</dd> <dt>

*UFormat* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opzioni di formattazione. Per un elenco completo di opzioni, vedere la documentazione relativa a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

</dd> <dt>

*lpDTParams* \[ in\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntatore a una struttura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) che specifica le opzioni di formattazione aggiuntive. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche. Se si specifica **DT \_ vCenter** o **DT \_ Bottom** , il valore restituito è l'offset dal **primo** membro di *LPRC* alla fine del testo disegnato se la funzione ha esito negativo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**DrawTextWrap** non viene esportato in base al nome o dichiarato in un'intestazione pubblica. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 415 da ComCtl32.dll per ottenere un puntatore a funzione.

Per ulteriori osservazioni, vedere [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 6,0 o successiva)</dt> </dl> |



 

