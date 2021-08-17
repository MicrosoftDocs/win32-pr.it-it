---
title: Funzione SaveSystemAcctInputSettings
description: Applica il layout della tastiera dell'utente e l'impostazione del servizio di testo all'hive degli account di sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Funzione SaveSystemAcctInputSettings Framework servizi di testo
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
ms.openlocfilehash: c60b9743ebbf54ce7189499f7295d44377c272b6d7cfcf5693259f12657bf06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875295"
---
# <a name="savesystemacctinputsettings-function"></a>Funzione SaveSystemAcctInputSettings

Applica il layout della tastiera dell'utente e l'impostazione del servizio di testo all'hive degli account di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Finestra padre per la finestra di dialogo di avviso. La finestra di dialogo di avviso non viene sempre visualizzata e viene visualizzata in modo appropriato. Se questo parametro è **NULL,** la finestra di dialogo di avviso non verrà visualizzata.

</dd> <dt>

*hSourceRegKey* \[ Pollici\]
</dt> <dd>

Chiave del Registro di sistema radice dell'impostazione utente da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | La funzione ha avuto esito positivo.<br/>   |
| <dl> <dt>**False**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

L'hive dell'account di sistema è HKEY \_ USERS \\ . DEFAULT, HKEY \_ USERS \\ S-1-5-19 e HKEY \_ USERS \\ S-1-5-20.

## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, pertanto è necessario ottenere un puntatore a questa funzione usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> [**L'uso errato di LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la DLL errata. Per informazioni su come caricare correttamente le DLL con versioni diverse di Microsoft Windows, vedere [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) (Ordine di ricerca della libreria a collegamento dinamico).

 


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

