---
description: Il metodo SetAsSingleton dell'oggetto SWbemObjectPath forza il percorso a un'istanza WMI singleton di una classe. Una classe singleton è una classe che non può mai avere più di un'istanza.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Metodo SWbemObjectPath.SetAsSingleton (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4a8a46566990021a4de4fca95b2b524cc7ddc1f5a797d7e3bffd0dc34ee52186
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568261"
---
# <a name="swbemobjectpathsetassingleton-method"></a>Metodo SWbemObjectPath.SetAsSingleton

Il **metodo SetAsSingleton** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) forza il percorso a un'istanza WMI singleton di una classe. Una classe singleton è una classe che non può mai avere più di un'istanza.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md). SWbemObjectPath

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **SetAsSingleton,** **l'oggetto Err** può contenere il codice di errore seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




