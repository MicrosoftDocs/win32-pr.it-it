---
description: Converte un percorso Microsoft MS-DOS in un URL in formato canonico.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Funzione MFCreateURLFromPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739249"
---
# <a name="mfcreateurlfrompath-function"></a>Funzione MFCreateURLFromPath

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono invece chiamare [UrlCreateFromPath.](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)\]

Converte un percorso Microsoft MS-DOS in un URL in formato canonico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszFilePath* \[ in, facoltativo\]
</dt> <dd>

Stringa con terminazione Null che contiene il percorso. La lunghezza massima della stringa è **INTERNET \_ MAX URL \_ \_ LENGTH**.

</dd> <dt>

*ppwszFileURL* \[ Cambio\]
</dt> <dd>

Riceve una stringa con terminazione Null che contiene l'URL. Il chiamante deve liberare la stringa chiamando [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La stringa specificata nel *parametro pwszFilePath* è già in formato URL. In questo caso, *pszFilePath* viene semplicemente copiato in *ppszFileURL* senza modifiche.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Funzione completata. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico Mfplat.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation funzioni](media-foundation-functions.md)
</dt> </dl>

 

 
