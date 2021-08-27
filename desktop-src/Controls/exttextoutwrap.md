---
title: Funzione ExtTextOutWrap
description: Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati. Facoltativamente, è possibile specificare le dimensioni da usare per il ritaglio, l'opacità o entrambi. Questa funzione esegue il wrapping di una chiamata a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Funzione ExtTextOutWrap Windows controlli
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934a8d203cf232a339db46e97783e87c075e5bb949ec5d23e20a7b1874ea6ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047271"
---
# <a name="exttextoutwrap-function"></a>Funzione ExtTextOutWrap

\[**ExtTextOutWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere stato modificato o non disponibile nelle versioni successive. È consigliabile usare [**ExtTextOut direttamente.**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)\]

Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati. Facoltativamente, è possibile specificare le dimensioni da usare per il ritaglio, l'opacità o entrambi. Questa funzione esegue il wrapping di una chiamata a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="syntax"></a>Sintassi


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hdc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Tipo: **int**

Coordinata x, in coordinate logiche, del punto di riferimento utilizzato per posizionare la stringa.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Tipo: **int**

Coordinata y, in coordinate logiche, del punto di riferimento utilizzato per posizionare la stringa.

</dd> <dt>

*uOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valori che specificano come usare il rettangolo definito dall'applicazione. Per un elenco completo delle opzioni, vedere [**ExtTextOut.**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)

</dd> <dt>

*lprc* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) facoltativa che specifica le dimensioni, in coordinate logiche, di un rettangolo utilizzato per il ritaglio, l'opacità o entrambi.

</dd> <dt>

*lpString* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer che contiene il testo da disegnare. Non è necessario che la stringa sia con terminazione zero, perché *cbCount* specifica la lunghezza della stringa.

</dd> <dt>

*cbCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza della stringa, in byte, a cui punta *lpString*.

</dd> <dt>

*lpDx* \[ Pollici\]
</dt> <dd>

Tipo: **const [**INT**](/windows/desktop/WinProg/windows-data-types) \***

Puntatore a una matrice facoltativa di valori che indicano la distanza tra le origini delle celle di caratteri adiacenti. Ad esempio, *le unità logiche lpDx* x separano le origini della cella di caratteri x e della cella \[ di caratteri \] (x + 1).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Restituisce un valore diverso da zero se la stringa viene disegnata correttamente. Tuttavia, se la versione ANSI di [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) viene chiamata con ETO GLYPH INDEX, la funzione restituisce TRUE anche se la funzione \_ \_ non esegue alcuna  operazione.

Se la funzione ha esito negativo, il valore restituito è zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**ExtTextOutWrap** non viene esportato per nome o dichiarato in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 417 da ComCtl32.dll ottenere un puntatore a funzione.

Per altre osservazioni, vedere [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 6.0 o successiva)</dt> </dl> |



 

