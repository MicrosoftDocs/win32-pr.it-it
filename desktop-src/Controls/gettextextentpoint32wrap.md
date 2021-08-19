---
title: Funzione GetTextExtentPoint32Wrap
description: Calcola la larghezza e l'altezza della stringa di testo specificata. Questa funzione esegue il wrapping di una chiamata a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Funzione GetTextExtentPoint32Wrap Windows controlli
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
ms.openlocfilehash: 0217d1708764ec33dd76ea35ff330f0d411697b5e9be3a6bd148377002a1f127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047211"
---
# <a name="gettextextentpoint32wrap-function"></a>Funzione GetTextExtentPoint32Wrap

\[**GetTextExtentPoint32Wrap** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive. È consigliabile usare [**direttamente GetTextExtentPoint.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)\]

Calcola la larghezza e l'altezza della stringa di testo specificata. Questa funzione esegue il wrapping di una [**chiamata a GetTextExtentPoint.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)

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

*hdc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle per il contesto di dispositivo.

</dd> <dt>

*lpString* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a un buffer che contiene il testo da disegnare. Non è necessario che la stringa sia con terminazione zero, perché *cbCount* specifica la lunghezza della stringa.

</dd> <dt>

*cbCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza, in byte, della stringa a cui punta *lpString*.

</dd> <dt>

*lpSize* \[ Cambio\]
</dt> <dd>

Tipo: **LPSIZE**

Quando questo metodo viene restituito, contiene un puntatore a una [**struttura SIZE**](/previous-versions//dd145106(v=vs.85)) contenente le dimensioni della stringa, in unità logiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Restituisce un valore diverso da zero in caso di esito positivo. in caso contrario, 0.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

**GetTextExtentPoint32Wrap** non viene esportato per nome o dichiarato in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 420 ComCtl32.dll ottenere un puntatore a funzione.

Per altre osservazioni, vedere [**GetTextExtentPoint.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                                  |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5.81 o successiva)</dt> </dl> |



 

