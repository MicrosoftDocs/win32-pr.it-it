---
title: InstallLayoutOrTipUserReg (funzione)
description: Abilita i layout di tastiera o i servizi di testo specificati per l'utente specificato.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Framework servizi di testo funzione InstallLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741626"
---
# <a name="installlayoutortipuserreg-function"></a>InstallLayoutOrTipUserReg (funzione)

Abilita i layout di tastiera o i servizi di testo specificati per l'utente specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
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

Percorso del registro di sistema dell'utente. Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .

</dd> <dt>

*pszSystemReg* \[ in, facoltativo\]
</dt> <dd>

Percorso del registro di sistema. Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .

</dd> <dt>

*pszSoftwareReg* \[ in, facoltativo\]
</dt> <dd>

Percorso del registro di sistema del software. Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .

</dd> <dt>

*PSZ* \[ in\]
</dt> <dd>

Stringa che rappresenta l'elenco di layout della tastiera o del profilo dei servizi di testo.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Oggetto bit che specifica i flag seguenti.

> [!Note]  
> Gli identificatori seguenti non sono definiti in un file di intestazione pubblico. È necessario utilizzare il valore esadecimale o \# definire gli identificatori. Ad esempio, per usare **la \_ disinstallazione di Ilot** , è necessario includere `#define ILOT_UNINSTALL 0x00000001` nel codice.

 



| Valore                                                                                                                                                                                                                                                                      | Significato                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**Ilot \_ Disinstalla**</dt> <dt>0x00000001</dt> </dl>                                           | Uguale a **Ilot \_ disabilitato**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**Ilot \_**</dt> <dt>0x00000002</dt> DEFPROFILE </dl>                                        | Imposta il layout o il suggerimento specificato come elemento predefinito.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**Ilot \_**</dt> <dt>0x00000020</dt> NOAPPLYTOCURRENTSESSION </dl> | L'impostazione viene salvata ma non viene applicata alla sessione corrente.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**Ilot \_**</dt> <dt>0x00000040</dt> CLEANINSTALL </dl>                                  | Disabilita tutti i layout di tastiera e i servizi di testo correnti.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**Ilot \_ 0x00000080 DISABILITAto**</dt> <dt></dt> </dl>                                              | Disabilita il layout di tastiera e il servizio di testo specificati.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                         | Descrizione                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl> | La funzione è stata completata.<br/>   |
| <dl> <dt>**FASE**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

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
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
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



 

