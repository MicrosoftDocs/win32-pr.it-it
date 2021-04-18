---
description: Converte un percorso Microsoft MS-DOS in un URL canonico.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath (funzione)
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
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308411"
---
# <a name="mfcreateurlfrompath-function"></a>MFCreateURLFromPath (funzione)

\[Questa API non è supportata e può essere modificata o non disponibile in futuro. Al contrario, le applicazioni devono chiamare [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Converte un percorso Microsoft MS-DOS in un URL canonico.

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

Stringa con terminazione null che contiene il percorso. La lunghezza massima della stringa è la **\_ \_ \_ lunghezza URL Internet Max**.

</dd> <dt>

*ppwszFileURL* \[ out\]
</dt> <dd>

Riceve una stringa con terminazione null che contiene l'URL. Il chiamante deve liberare la stringa chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La stringa specificata nel parametro *pwszFilePath* è già in formato URL. In questo caso, *pszFilePath* viene semplicemente copiato in *ppszFileURL* senza modifiche.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Funzione completata. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Mfplat.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
