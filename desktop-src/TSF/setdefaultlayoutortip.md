---
title: SetDefaultLayoutOrTip (funzione)
description: Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito dell'utente corrente.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Framework servizi di testo funzione SetDefaultLayoutOrTip
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119299"
---
# <a name="setdefaultlayoutortip-function"></a>SetDefaultLayoutOrTip (funzione)

Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito dell'utente corrente.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PSZ* \[ in\]
</dt> <dd>

Stringa che rappresenta un elenco di layout della tastiera o un elenco di profili di servizi di testo.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Oggetto bit che specifica i flag seguenti.

> [!Note]  
> Gli identificatori seguenti non sono definiti in un file di intestazione pubblico. È necessario utilizzare il valore esadecimale o \# definire gli identificatori. Ad esempio, per usare SDLOT \_ NOAPPLYTOCURRENTSESSION, è necessario includere \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 nel codice.

 



| Valore                                                                                                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_**</dt> <dt>0x00000001</dt> NOAPPLYTOCURRENTSESSION </dl> | Archivia l'impostazione nel registro di sistema, ma la dose non aggiorna l'impostazione della tastiera di runtime della sessione corrente. Se il percorso del registro di sistema alternativo è impostato in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), questo flag deve essere impostato.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_**</dt> <dt>0x00000002</dt> APPLYTOCURRENTTHREAD </dl>          | Applica immediatamente l'impostazione nel thread corrente.<br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | La funzione è stata completata.<br/>   |
| <dl> <dt>**FALSE**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Il formato della stringa dell'elenco di layout è:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

Il formato stringa dell'elenco profilo servizio di testo è:

<LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Di seguito è riportato un esempio di un valore per il parametro *PSZ* :


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

