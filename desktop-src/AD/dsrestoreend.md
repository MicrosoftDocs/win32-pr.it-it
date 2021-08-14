---
title: Funzione DsRestoreEnd (Ntdsbcli.h)
description: Chiamato per terminare un'operazione di ripristino.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Funzione DsRestoreEnd in Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fbea2559517f6cc541d89817ab32c9d1992da4907f399b94830b41b1b0c1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191817"
---
# <a name="dsrestoreend-function"></a>Funzione DsRestoreEnd

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare [Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsRestoreEnd** viene chiamata per terminare un'operazione di ripristino.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto [**con la funzione DsRestorePrepare.**](dsrestoreprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo oppure un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i codici di errore possibili.

<dl> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*hbc* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **funzione DsRestoreEnd** chiude gli handle di associazione in sospeso ed esegue un'operazione di pulizia dopo un tentativo di ripristino.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                               |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[Ripristino di un server Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

