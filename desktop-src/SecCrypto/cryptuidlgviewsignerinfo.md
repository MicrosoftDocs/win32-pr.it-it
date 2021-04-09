---
description: Visualizza una finestra di dialogo contenente le informazioni sul firmatario per un messaggio firmato.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Funzione CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878954"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>Funzione CryptUIDlgViewSignerInfo

\[La funzione **CryptUIDlgViewSignerInfo** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

La funzione **CryptUIDlgViewSignerInfo** Visualizza una finestra di dialogo contenente le informazioni sul firmatario per un messaggio firmato.

> [!Note]  
> Questa funzione non è dichiarata in un file di intestazione pubblicato. Per usare questa struttura, dichiararla nel formato esatto indicato.

## <a name="syntax"></a>Sintassi


```C++
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcvsi* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CRYPTUI \_ VIEWSIGNERINFO \_ struct**](cryptui-viewsignerinfo-struct.md) che contiene le informazioni sul firmatario da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce un valore diverso da zero in caso di esito positivo e zero in caso di errore. Per informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

I codici di errore possibili restituiti da [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) includono ma non sono limitati a quanto segue.



| Codice restituito                                                                                   | Descrizione                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o più argomenti non sono validi.<br/>  |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Si è verificato un errore di allocazione della memoria.<br/> |

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                        |
| Fine del supporto<br/> | \[Solo app desktop di Windows 7\]<br/>                                                       |
| Libreria<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Nomi Unicode e ANSI<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) e **CryptUIDlgViewSignerInfoA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_struct CRYPTUI VIEWSIGNERINFO \_**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
