---
title: EnumLayoutOrTipForSetup (funzione)
description: Enumera i layout di tastiera e i servizi di testo installati dell'interfaccia utente o della OOBE del programma di installazione.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Framework servizi di testo funzione EnumLayoutOrTipForSetup
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301346"
---
# <a name="enumlayoutortipforsetup-function"></a>EnumLayoutOrTipForSetup (funzione)

Enumera i layout di tastiera e i servizi di testo installati dell'interfaccia utente o della OOBE del programma di installazione.

## <a name="syntax"></a>Sintassi


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LangID* \[ in\]
</dt> <dd>

ID lingua dell'elemento da enumerare.

</dd> <dt>

*pLayoutOrTip* \[ out\]
</dt> <dd>

Puntatore al buffer che riceve la matrice di strutture LAYOUTORTIP. Può essere **null** per ottenere il numero di elementi.

</dd> <dt>

*uBufLength* \[ in\]
</dt> <dd>

Lunghezza del buffer a cui punta *pLayoutOrTip*. Viene ignorato se *pLayoutOrTip* è **null**.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Non usato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *pLayoutOrTip* è **null**, il numero di elementi della tastiera registrati nel sistema; in caso contrario, il numero di elementi della tastiera che vengono copiati in *pLayoutOrTip*.

## <a name="remarks"></a>Commenti

Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta. Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

La definizione di LAYOUTORTIP è:

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

