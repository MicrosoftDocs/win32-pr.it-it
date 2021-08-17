---
description: Il metodo GetObjectText \_ dell'oggetto SWbemObject restituisce un rendering testuale dell'oggetto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: SWbemObject.GetObjectText_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d33e4f3f530bf7d9bda2e228243026de7d3768efb668cf6c8683690e8127f65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992061"
---
# <a name="swbemobjectgetobjecttext_-method"></a>Metodo SWbemObject.GetObjectText \_

Il **metodo \_ GetObjectText** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un rendering testuale dell'oggetto. Questo oggetto può essere usato per visualizzare il contenuto di un oggetto. Attualmente, solo la sintassi MOF è supportata come formato di output. Si noti che il testo MOF restituito non contiene tutte le informazioni sull'oggetto. Il testo MOF contiene solo informazioni sufficienti per il compilatore MOF per poter ri-creare l'oggetto originale. Ad esempio, non sono disponibili informazioni sui qualificatori propagati o sulle proprietà della classe padre.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Riservato e deve essere 0 (zero) se specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, questo metodo restituisce una stringa contenente il testo di output.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo GetObjectText, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="examples"></a>Esempio

Il codice seguente, tratto dall'esempio di codice VBScript Elencare la definizione di una classe WMI in formato [MOF](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) in TechNet Gallery, recupera e visualizza la rappresentazione testuale di una definizione di classe WMI nella sintassi MOF (Managed Object Format).


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




