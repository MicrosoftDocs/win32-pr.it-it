---
description: Il metodo GetObjectText dell'oggetto SWbemLastError restituisce un rendering testuale dell'oggetto \_ in Managed Object Format (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: SWbemLastError.GetObjectText_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7f935457c6fa6566d69c10b6cb5cade914e6e81c175f7451cc6eaff5268358e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679591"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>Metodo SWbemLastError.GetObjectText \_

Il **metodo \_ GetObjectText** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un rendering testuale dell'oggetto in [Managed Object Format (MOF).](managed-object-format--mof-.md) Questo oggetto MOF può essere usato per visualizzare il contenuto di un oggetto. Si noti che il testo MOF restituito non contiene tutte le informazioni sull'oggetto, ma solo informazioni sufficienti per il compilatore MOF per poter creare nuovamente l'oggetto originale. Ad esempio, non sarà possibile trovare informazioni sui qualificatori propagati o sulle proprietà della classe padre.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Questo parametro è riservato e deve essere 0 (zero) se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo metodo restituisce una stringa che contiene il testo di output.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **GetObjectText, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




