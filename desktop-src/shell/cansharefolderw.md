---
description: Consente di determinare se visualizzare l'opzione Condividi questa cartella nella visualizzazione Web.
title: Funzione CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032869"
---
# <a name="cansharefolderw-function"></a>Funzione CanShareFolderW

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Consente di determinare se visualizzare l'opzione Condividi **questa cartella** nella visualizzazione Web.

## <a name="syntax"></a>Sintassi


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPath* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il percorso della cartella da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **STDAPI**

I valori restituiti includono quanto segue.



| Codice/valore restituito                                                                        | Descrizione                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | Il percorso a cui punta *pszPath* specifica una cartella che può essere condivisa.<br/>    |
| <dl> <dt>**S \_ FALSE**</dt> </dl>  | Il percorso a cui punta *pszPath* specifica una cartella che non può essere condivisa.<br/> |
| <dl> <dt>Errore HRESULT</dt> </dl> | un errore.<br/>                                                     |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file lib. Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
