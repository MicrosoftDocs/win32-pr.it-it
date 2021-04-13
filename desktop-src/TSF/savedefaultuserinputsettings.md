---
title: SaveDefaultUserInputSettings (funzione)
description: Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive utente predefinito.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Framework servizi di testo funzione SaveDefaultUserInputSettings
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400412"
---
# <a name="savedefaultuserinputsettings-function"></a>SaveDefaultUserInputSettings (funzione)

Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive utente predefinito.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Finestra padre per la finestra di dialogo di avviso. La finestra di dialogo di avviso non è sempre visualizzata e viene visualizzata in modo appropriato. Se questo parametro è NULL, la finestra di dialogo di avviso non verrà visualizzata.

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



 

## <a name="examples"></a>Esempio

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
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



 

