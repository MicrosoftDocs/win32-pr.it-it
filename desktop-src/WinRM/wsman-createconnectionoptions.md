---
title: Metodo WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crea un oggetto ConnectionOptions che specifica il nome utente e la password utilizzati durante la creazione di una sessione.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateConnectionOptions
- Metodo CreateConnectionOptions Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873541"
---
# <a name="wsmancreateconnectionoptions-method"></a>WSMan. CreateConnectionOptions, metodo

Crea un oggetto [**ConnectionOptions**](connectionoptions.md) che specifica il nome utente e la password utilizzati durante la creazione di una sessione.

## <a name="syntax"></a>Sintassi


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Oggetto [**ConnectionOptions**](connectionoptions.md) utilizzato per specificare una coppia di nome utente e password utilizzata per identificare un utente per l'autenticazione.

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, viene usata la sintassi seguente.


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





