---
title: QueryLayoutOrTipStringUserReg (funzione)
description: Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili dei servizi di testo del percorso del registro di sistema specificato.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Framework servizi di testo funzione QueryLayoutOrTipStringUserReg
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302237"
---
# <a name="querylayoutortipstringuserreg-function"></a>QueryLayoutOrTipStringUserReg (funzione)

Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili dei servizi di testo del percorso del registro di sistema specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszUserReg* \[ in\]
</dt> <dd>

Percorso del registro di sistema dell'utente. Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .

</dd> <dt>

*pszSystemReg* \[ in\]
</dt> <dd>

Percorso del registro di sistema. Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .

</dd> <dt>

*pszSoftwareReg* \[ in\]
</dt> <dd>

Percorso del registro di sistema del software. Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .

</dd> <dt>

*PSZ* \[ in\]
</dt> <dd>

Stringa che rappresenta un elenco di layout della tastiera o un elenco di profili di servizi di testo.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Tutti i layout o i profili definiti in **PSZ** sono validi.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più layout o profili definiti in **PSZ** non sono validi.<br/> |



 

## <a name="remarks"></a>Commenti

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Il formato della stringa dell'elenco di layout è:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

Il formato stringa dell'elenco profilo servizio di testo è:

<LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Di seguito è riportato un esempio di un valore per il parametro *PSZ* :

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

