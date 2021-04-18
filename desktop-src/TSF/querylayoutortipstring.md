---
title: QueryLayoutOrTipString (funzione)
description: Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili di servizi di testo.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Framework servizi di testo funzione QueryLayoutOrTipString
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302238"
---
# <a name="querylayoutortipstring-function"></a>QueryLayoutOrTipString (funzione)

Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili di servizi di testo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
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

Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Tutti i layout o i profili definiti in *PSZ* sono validi.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più layout o profili definiti in *PSZ* non sono validi.<br/> |



 

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



 

