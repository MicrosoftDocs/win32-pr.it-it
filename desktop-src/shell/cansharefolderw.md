---
description: Utilizzato per determinare se visualizzare l'opzione Condividi questa cartella nella visualizzazione Web.
title: CanShareFolderW (funzione)
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525404"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW (funzione)

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Utilizzato per determinare se visualizzare l'opzione **Condividi questa cartella** nella visualizzazione Web.

## <a name="syntax"></a>Sintassi


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPath* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il percorso della cartella da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **STDAPI**

I valori restituiti includono i seguenti.



| Codice/valore restituito                                                                        | Descrizione                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>     | Il percorso a cui punta *pszPath* specifica una cartella che può essere condivisa.<br/>    |
| <dl> <dt>**S \_ false**</dt> </dl>  | Il percorso a cui punta *pszPath* specifica una cartella che non può essere condivisa.<br/> |
| <dl> <dt>Errore HRESULT</dt> </dl> | un errore.<br/>                                                     |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file con estensione LIB. Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
