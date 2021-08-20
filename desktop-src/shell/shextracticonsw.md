---
description: Crea una matrice di handle per le icone estratte da un file specificato.
title: Funzione SHExtractIconsW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 06ebb05717f663fe8b18c75135479ddd09b12dadac6733de9e408cd5b91a3e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047154"
---
# <a name="shextracticonsw-function"></a>Funzione SHExtractIconsW

\[**SHExtractIconsW** è disponibile tramite Windows XP Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive.\]

Crea una matrice di handle per le icone estratte da un file specificato.

## <a name="syntax"></a>Sintassi


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszFileName* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore al nome del file da cui estrarre le icone.

</dd> <dt>

*nIconIndex* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Indice della prima icona da estrarre dalla risorsa denominata in *pszFileName*.

</dd> <dt>

*cxIcon* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Larghezza desiderata dell'icona. Vedere la sezione Osservazioni.

</dd> <dt>

*cyIcon* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Altezza desiderata dell'icona. Vedere la sezione Osservazioni.

</dd> <dt>

*phIcon* \[ Cambio\]
</dt> <dd>

Tipo: **HICON \***

Quando questa funzione viene restituita, contiene un puntatore alla matrice di handle di icona.

</dd> <dt>

*pIconId* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Quando questa funzione viene restituita, contiene un puntatore all'identificatore di risorsa dell'icona estratta più adatta al dispositivo di visualizzazione corrente. Se non è disponibile alcun identificatore per questo formato, contiene 0xFFFFFFFF. Se non è possibile ottenere alcun identificatore per qualsiasi altro motivo, restituisce zero.

</dd> <dt>

*nIcons* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero di icone da estrarre dalla risorsa denominata in *pszFileName*. Questo parametro è valido solo quando la risorsa è un .exe o .dll file.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Flag che controllano questa funzione. Per i valori possibili, *vedere il parametro fuLoad* della [**funzione LoadImage.**](/windows/win32/api/winuser/nf-winuser-loadimagea)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UINT**

Valore diverso da zero in caso di esito positivo. in caso contrario, zero.

## <a name="remarks"></a>Commenti

**SHExtractIconsW** estrae dai tipi di file seguenti.

-   Eseguibile (con estensione exe)
-   DLL (.dll)
-   Icona (.ico)
-   Cursore (.cur)
-   Cursore animato (.ani)
-   Bitmap (.bmp)

Estrazioni da Windows 3. *Sono* supportati anche i file eseguibili a 16 bit (.exe o .dll).

I *parametri cxIcon* *e cyIcon* specificano le dimensioni delle icone da estrarre. È possibile estrarre due dimensioni tramite ogni parametro suddividendo il valore tra i valori LOWORD e HIWORD. Inserire la prima dimensione desiderata nel valore LOWORD del parametro e la seconda dimensione in HIWORD. MakeLONG [](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) per *cxIcon* e *cyIcon,* ad esempio, estrae icone con dimensioni di 24 e 48.

Il processo chiamante è responsabile dell'eliminazione di tutte le icone estratte tramite questa funzione chiamando la [**funzione DestroyIcon.**](/windows/win32/api/winuser/nf-winuser-destroyicon)

**SHExtractIconsW** non viene esportato per nome o dichiarato in un file di intestazione pubblico. Per usarlo, è necessario dichiarare un prototipo corrispondente e usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per richiedere un puntatore a funzione da Shell32.dll che può essere usato per chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 
