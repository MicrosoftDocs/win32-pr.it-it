---
title: Funzione SetDefaultLayoutOrTipUserReg
description: Imposta il layout di tastiera specificato o un servizio di testo come elemento di input predefinito del registro utenti.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Funzione SetDefaultLayoutOrTipUserReg Framework servizi di testo
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 340e21d8d7416d72361a0e505029500b9a7dde3e53d3388c9311ae3351345c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875285"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>Funzione SetDefaultLayoutOrTipUserReg

Imposta il layout di tastiera specificato o un servizio di testo come elemento di input predefinito del registro utenti.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszUserReg* \[ in, facoltativo\]
</dt> <dd>

Percorso del Registro di sistema dell'utente. Se questo parametro è **NULL,** viene usato HKEY \_ CURRENT \_ USER.

</dd> <dt>

*pszSystemReg* \[ in, facoltativo\]
</dt> <dd>

Percorso del Registro di sistema. Se questo parametro è **NULL,** viene usato HKEY \_ LOCAL MACHINE \_ \\ System.

</dd> <dt>

*pszSoftwareReg* \[ in, facoltativo\]
</dt> <dd>

Percorso del Registro di sistema del software. Se questo parametro è **NULL,** viene usato HKEY \_ LOCAL MACHINE \_ \\ Software.

</dd> <dt>

*psz* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta l'elenco di layout di tastiera o l'elenco di profili dei servizi di testo.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Campo di bit che specifica i flag seguenti:

> [!Note]  
> Gli identificatori seguenti non sono definiti in un file di intestazione pubblico. È necessario usare il valore esadecimale o \# definire gli identificatori. Ad esempio, per usare SDLOT NOAPPLYTOCURRENTSESSION è necessario includere nel codice il 0x00000001 \_ \# SDLOT \_ NOAPPLYTOCURRENTSESSION.

 



| Valore                                                                                                                                                                                                                                                                         | Significato                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Archivia l'impostazione nel Registro di sistema, ma non aggiorna l'impostazione della tastiera di runtime della sessione corrente. Se il percorso alternativo del Registro di sistema è impostato in **SetDefaultLayoutOrTipUserReg,** questo flag deve essere impostato.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Applica l'impostazione immediatamente al thread corrente.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | La funzione ha avuto esito positivo.<br/>   |
| <dl> <dt>**False**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Il formato stringa dell'elenco di layout è:

<LangID 1>:<KLID 1>; \[ ...<LangID N>:<KLID N>

Il formato della stringa dell'elenco di profili del servizio di testo è:

<LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx};

Di seguito è riportato un esempio di valore per il *parametro psz:*


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, pertanto è necessario ottenere un puntatore a questa funzione usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> [**L'uso non corretto di LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la DLL errata. Per informazioni su come caricare correttamente le DLL con versioni diverse di Microsoft Windows, vedere [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) (Ordine di ricerca della libreria a collegamento dinamico).

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

