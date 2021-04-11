---
title: ExtTextOutWrap (funzione)
description: Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati. Facoltativamente, è possibile specificare le dimensioni da utilizzare per il ritaglio, l'opacità o entrambi. Questa funzione esegue il wrapping di una chiamata a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Controlli Windows per la funzione ExtTextOutWrap
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
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119083"
---
# <a name="exttextoutwrap-function"></a>ExtTextOutWrap (funzione)

\[**ExtTextOutWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. Si consiglia invece di usare direttamente [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .\]

Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati. Facoltativamente, è possibile specificare le dimensioni da utilizzare per il ritaglio, l'opacità o entrambi. Questa funzione esegue il wrapping di una chiamata a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

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

*HDC* \[ in\]
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

*uOptions* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valori che specificano come usare il rettangolo definito dall'applicazione. Per un elenco completo delle opzioni, vedere [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .

</dd> <dt>

*LPRC* \[ in\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _

Puntatore a una struttura facoltativa [_ *Rect* *](/previous-versions//dd162897(v=vs.85)) che specifica le dimensioni, in coordinate logiche, di un rettangolo utilizzato per il ritaglio, l'opacità o entrambi.

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer contenente il testo da disegnare. La stringa non deve essere con terminazione zero, poiché *cbCount* specifica la lunghezza della stringa.

</dd> <dt>

*cbCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza della stringa, in byte, a cui punta *lpString*.

</dd> <dt>

*lpDx* \[ in\]
</dt> <dd>

Tipo: **const [**int**](/windows/desktop/WinProg/windows-data-types) \** _

Puntatore a una matrice di valori facoltativa che indica la distanza tra le origini delle celle di caratteri adiacenti. Ad esempio, \[ \] le unità logiche _lpDx * x separano le origini della cella di tipo carattere x e della cella (x + 1).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Restituisce un valore diverso da zero se la stringa viene disegnata correttamente. Tuttavia, se la versione ANSI di [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) viene chiamata con l' \_ indice del glifo Eto \_ , la funzione restituisce **true** anche se la funzione non esegue alcuna operazione.

Se la funzione ha esito negativo, il valore restituito è zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**ExtTextOutWrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 417 da ComCtl32.dll per ottenere un puntatore a funzione.

Per ulteriori osservazioni, vedere [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 6,0 o successiva)</dt> </dl> |



 

