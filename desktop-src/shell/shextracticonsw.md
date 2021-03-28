---
description: Crea una matrice di handle per le icone estratte da un file specificato.
title: SHExtractIconsW (funzione)
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
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994805"
---
# <a name="shextracticonsw-function"></a>SHExtractIconsW (funzione)

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

*pszFileName* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore al nome file da cui estrarre le icone.

</dd> <dt>

*nIconIndex* \[ in\]
</dt> <dd>

Tipo: **int**

Indice della prima icona da estrarre dalla risorsa denominata in *pszFileName*.

</dd> <dt>

*cxIcon* \[ in\]
</dt> <dd>

Tipo: **int**

Larghezza desiderata dell'icona. Vedere la sezione Osservazioni.

</dd> <dt>

*cyIcon* \[ in\]
</dt> <dd>

Tipo: **int**

Altezza desiderata dell'icona. Vedere la sezione Osservazioni.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \** _

Quando la funzione restituisce un risultato, contiene un puntatore alla matrice di handle di icona.

</dd> <dt>

_pIconId * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Quando la funzione restituisce un risultato, contiene un puntatore all'identificatore di risorsa dell'icona estratta che meglio si adatta al dispositivo di visualizzazione corrente. Se non è disponibile alcun identificatore per questo formato, contiene 0xFFFFFFFF. Se non è possibile ottenere un identificatore per qualsiasi altro motivo, restituisce zero.

</dd> <dt>

_nIcons * \[ in\]
</dt> <dd>

Tipo: **uint**

Il numero di icone da estrarre dalla risorsa denominata in *pszFileName*. Questo parametro è valido solo se la risorsa è un file con estensione exe o dll.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Tipo: **uint**

Flag che controllano questa funzione. Per i valori possibili, vedere il parametro *fuLoad* della funzione [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Valore diverso da zero se ha esito positivo; in caso contrario, zero.

## <a name="remarks"></a>Commenti

**SHExtractIconsW** estrae dai tipi di file seguenti.

-   Eseguibile (con estensione exe)
-   DLL (. dll)
-   Icona (. ico)
-   Cursore (. cur)
-   Cursore animato (. ani)
-   Bitmap (.bmp)

Estrazioni da Windows 3. sono supportati anche file eseguibili *a 16 bit* (con estensione exe o dll).

I parametri *cxIcon* e *cyIcon* specificano le dimensioni delle icone da estrarre. È possibile estrarre due dimensioni tramite ogni parametro suddividendo il valore tra il relativo LOWORD e HIWORD. Inserire la prima dimensione desiderata nell'LOWORD del parametro e la seconda dimensione in HIWORD. Ad esempio, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) per *cxIcon* e *cyIcon* estrae entrambe le icone di dimensioni 24 e 48.

Il processo chiamante è responsabile dell'eliminazione di tutte le icone estratte tramite questa funzione chiamando la funzione [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .

**SHExtractIconsW** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico. Per usarlo, è necessario dichiarare un prototipo corrispondente e usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per richiedere un puntatore a funzione da Shell32.dll che può essere usato per chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 
