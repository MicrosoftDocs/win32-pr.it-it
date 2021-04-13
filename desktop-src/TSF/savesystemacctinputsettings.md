---
title: SaveSystemAcctInputSettings (funzione)
description: Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive degli account di sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Framework servizi di testo funzione SaveSystemAcctInputSettings
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400280"
---
# <a name="savesystemacctinputsettings-function"></a>SaveSystemAcctInputSettings (funzione)

Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive degli account di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Finestra padre per la finestra di dialogo di avviso. La finestra di dialogo di avviso non è sempre visualizzata e viene visualizzata in modo appropriato. Se questo parametro è **null**, la finestra di dialogo di avviso non verrà visualizzata.

</dd> <dt>

*hSourceRegKey* \[ in\]
</dt> <dd>

Chiave del registro di sistema radice dell'impostazione utente da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | La funzione è stata completata.<br/>   |
| <dl> <dt>**FALSE**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

L'account di sistema hive è HKEY \_ Users \\ . DEFAULT, HKEY \_ Users \\ s-1-5-19 e HKEY \_ Users \\ s-1-5-20.

## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
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



 

