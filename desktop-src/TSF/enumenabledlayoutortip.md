---
title: EnumEnabledLayoutOrTip (funzione)
description: Enumera tutti i layout di tastiera abilitati o i servizi di testo dell'impostazione utente specificata.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Framework servizi di testo funzione EnumEnabledLayoutOrTip
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301570"
---
# <a name="enumenabledlayoutortip-function"></a>EnumEnabledLayoutOrTip (funzione)

Enumera tutti i layout di tastiera abilitati o i servizi di testo dell'impostazione utente specificata.

## <a name="syntax"></a>Sintassi


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
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

*pLayoutOrTipProfile* \[ out\]
</dt> <dd>

Puntatore al buffer che riceve la matrice LAYOUTORTIPPROFILE.

</dd> <dt>

*uBufLength* \[ in\]
</dt> <dd>

Lunghezza del buffer a cui punta *pLayoutOrTipProfile*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *pLayoutOrTipProfile* è **null**, il numero di elementi della tastiera abilitati nell'impostazione utente; in caso contrario, il numero di elementi della tastiera che vengono copiati in *pLayoutOrTipProfile*.

Per i linguaggi IME (Input Method Editor), vengono restituiti tutti gli IME, anche quando è abilitato un solo IME. Se, ad esempio, per un utente è abilitato il nuovo IME rapido, la funzione **EnumEnabledLayoutOrTip** restituisce tutti i 5 IME cht.

## <a name="remarks"></a>Commenti

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

La definizione di LAYOUTORTIPPROFILE è:

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

