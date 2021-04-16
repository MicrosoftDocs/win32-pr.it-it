---
title: Funzione TF_InvalidAssemblyListCacheIfExist
description: La \_ funzione TF InvalidAssemblyListCacheIfExist invalida la cache di descrizione del processore di input del testo.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Framework servizi di testo TF_InvalidAssemblyListCacheIfExist funzione
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517571"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a>\_Funzione TF InvalidAssemblyListCacheIfExist

La funzione **tf \_ InvalidAssemblyListCacheIfExist** invalida la cache di descrizione del processore di input del testo. Non è necessario chiamare questa funzione se il programma di installazione del processore di input richiede il riavvio o l'accesso. La cache è valida fino a quando l'utente non si disconnette.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | La funzione è stata completata.<br/>   |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| DLL<br/>                      | <dl> <dt>Msctf.dll</dt> </dl> |



 

