---
title: Funzione DrawTextWrap
description: Disegna testo formattato nel rettangolo specificato. Formatta il testo in base al metodo specificato (espansione delle tabulazioni, giustificazione dei caratteri, interruzione delle righe e così via). Questa funzione esegue il wrapping di una chiamata a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Funzione DrawTextWrap Windows controlli
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
ms.openlocfilehash: dcbd504955b6ae772ffb3db7bc4cc0223215d6d9ecf880fe7d7e3aa359c992ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878291"
---
# <a name="drawtextwrap-function"></a>Funzione DrawTextWrap

\[**DrawTextWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. È consigliabile usare [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) direttamente.\]

Disegna testo formattato nel rettangolo specificato. Formatta il testo in base al metodo specificato (espansione delle tabulazioni, giustificazione dei caratteri, interruzione delle righe e così via). Questa funzione esegue il wrapping di una chiamata a [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

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

*hdc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer che contiene il testo da disegnare. Se il *parametro nCount* è -1, la stringa deve avere terminazione Null.

Se *uFormat* include DT MODIFYSTRING, la funzione potrebbe aggiungere fino a \_ quattro caratteri aggiuntivi a questa stringa. Il buffer che contiene la stringa deve essere sufficientemente grande da contenere questi caratteri aggiuntivi.

</dd> <dt>

*nCount* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Lunghezza della stringa a cui punta *lpString.* Se *nCount* è -1, si presuppone che il parametro *lpString* sia un puntatore a una stringa con terminazione Null e [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcola automaticamente il numero di caratteri.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.

</dd> <dt>

*uFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opzioni di formattazione. Per un elenco completo delle opzioni, vedere la documentazione relativa a [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

</dd> <dt>

*lpDTParams* \[ Pollici\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntatore a una [**struttura DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) che specifica opzioni di formattazione aggiuntive. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche. Se **si specifica DT \_ VCENTER** o **DT \_ BOTTOM,**  il valore restituito è l'offset dal membro superiore di *lprc* alla fine del testo disegnato Se la funzione ha esito negativo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**DrawTextWrap non** viene esportato per nome o dichiarato in un'intestazione pubblica. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 415 da ComCtl32.dll ottenere un puntatore a funzione.

Per altre osservazioni, vedere [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                                 |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 6.0 o successiva)</dt> </dl> |



 

