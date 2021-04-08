---
description: Restituisce una rappresentazione XML di un oggetto o di un'istanza di. Il file di testo è formattato nel formato XML specificato come indicato in WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Metodo SWbemObjectEx.GetText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058219"
---
# <a name="swbemobjectexgettext_-method"></a>Metodo SWbemObjectEx. GetText \_

Il metodo **gettext \_** dell'oggetto [**SWBEMOBJECTEX**](swbemobjectex.md) restituisce una rappresentazione XML di un oggetto o di un'istanza di. Il file di testo è formattato nel formato XML specificato come indicato in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iTextFormat* \[ in\]
</dt> <dd>

Obbligatorio. Valore di [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) che specifica il formato XML risultante.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Flag di operazione riservati. Il valore predefinito è 0 (zero).

</dd> <dt>

*objWbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che imposta il contesto per l'operazione. Il valore predefinito è Null. Per ulteriori informazioni sulle coppie nome/valore consentite, vedere la sezione Osservazioni di seguito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **gettext \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Il formato richiesto non è stato trovato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Uno dei parametri della chiamata non è corretto.

</dd> <dt>

**wbemErrCriticalError** -2147749898 (0x8004100a)
</dt> <dd>

Si è verificato un errore interno, irreversibile e inaspettato. Segnalare l'errore al Servizio Supporto Tecnico Microsoft.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si costruisce il [**SWbemNamedValueSet**](swbemnamedvalueset.md), sono consentite solo le seguenti coppie nome/valore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Valore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>true</strong>, nel codice XML risultante sono presenti solo metodi e proprietà definite localmente. Il valore predefinito è <strong>false</strong>.<br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>true</strong>, i qualificatori delle classi, delle istanze, delle proprietà e dei metodi sono inclusi nel codice XML risultante. Il valore predefinito è <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> Il valore predefinito è 0 (zero). I valori possibili sono:<br/>
<ul>
<li>0: un <CLASS> <INSTANCE> elemento o viene creato a seconda che l'oggetto sia una classe o un'istanza.</li>
<li>1: <VALUE.NAMEDOBJECT> viene generato un elemento.</li>
<li>2: <VALUE.OBJECTWITHLOCALPATH> viene generato un elemento.</li>
<li>3: <VALUE.OBJECTWITHPATH> viene generato un elemento.</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> Se <strong>true</strong>, le proprietà di sistema, come __NAMESPACE, sono escluse dall'output.<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> Se <strong>true</strong>, l'attributo Origin della classe viene impostato negli <PROPERTY> <METHOD> elementi e. Il valore predefinito è <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni sulla creazione di un [**SWbemNamedValueSet**](swbemnamedvalueset.md), vedere [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).

## <a name="examples"></a>Esempio

Nello script seguente viene illustrato come ottenere una rappresentazione XML della definizione della classe [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) . Specificando una particolare istanza di **\_ BIOS Win32**, è possibile ottenere i dati dell'oggetto in formato XML.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTEX CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMOBJECTEX IID<br/>                                                          |



 

