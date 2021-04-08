---
title: MirrorIcon (funzione)
description: Inverte le icone (mirror) in modo che vengano visualizzate correttamente in un contesto di dispositivo con mirroring.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Controlli Windows per la funzione MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047993"
---
# <a name="mirroricon-function"></a>MirrorIcon (funzione)

\[**MirrorIcon** è disponibile tramite Windows XP con Service Pack 2 (SP2). Potrebbe essere modificato o non disponibile nelle versioni successive.\]

Inverte le icone (mirror) in modo che vengano visualizzate correttamente in un contesto di dispositivo con mirroring.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phIconSmall* \[ in, out, facoltativo\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Puntatore all'handle dell'icona che fa riferimento a una versione ridotta di un'icona.

</dd> <dt>

_phIconLarge * \[ in, out, facoltativo\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Puntatore all'handle dell'icona che fa riferimento a una versione di grandi dimensioni di un'icona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se l'operazione ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

**MirrorIcon** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico. Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 414 da ComCtl32.dll per ottenere un puntatore a funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5,81 o successiva)</dt> </dl> |



 

