---
title: Metodo WSMan.CreateConnectionOptions (WSManDisp.h)
description: Crea un oggetto ConnectionOptions che specifica il nome utente e la password usati durante la creazione di una sessione.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Metodo CreateConnectionOptions Windows Gestione remota
- Metodo CreateConnectionOptions Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo CreateConnectionOptions
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
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742668"
---
# <a name="wsmancreateconnectionoptions-method"></a>Metodo WSMan.CreateConnectionOptions

Crea un [**oggetto ConnectionOptions**](connectionoptions.md) che specifica il nome utente e la password usati durante la creazione di una sessione.

## <a name="syntax"></a>Sintassi


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Oggetto [**ConnectionOptions**](connectionoptions.md) usato per specificare una coppia di nome utente e password usata per identificare un utente per l'autenticazione.

## <a name="remarks"></a>Commenti

La sintassi seguente viene usata per chiamare questo metodo.


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





