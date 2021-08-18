---
description: Aggiorna i dati per gli oggetti che dispongono di dati forniti da un provider di prestazioni, ad esempio le classi dei contatori delle prestazioni. È possibile ottenere dati aggiornati più rapidamente e senza una chiamata a SWbemServices.Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: SWbemObjectEx.Refresh_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6763607d2b5f29d32e722e5a1159a1fc276e546c4af9c2e5da10b1d4b2f08235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991941"
---
# <a name="swbemobjectexrefresh_-method"></a>Metodo SWbemObjectEx.Refresh \_

Il **\_ metodo Refresh** di [**SWbemObjectEx**](swbemobjectex.md) aggiorna i dati per gli oggetti con dati forniti da un provider di prestazioni, ad esempio le classi del [contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes). È possibile ottenere dati aggiornati più rapidamente e senza una chiamata a [**SWbemServices.Get \_**](swbemservices-get.md).

Per altre informazioni su questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Flag di operazione riservati che, se specificati, devono essere 0 (zero).

</dd> <dt>

*objWbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che imposta il contesto per l'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Refresh, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Il provider ha avuto esito negativo internamente, anche se l'operazione è valida.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

Il formato richiesto non è stato trovato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Uno dei parametri della chiamata non è corretto.

</dd> <dt>

**wbemErrRefresherBusy** - 2147749975 (0x80041057)
</dt> <dd>

L'aggiornamento è impegnato in un'altra operazione.

</dd> <dt>

**wbemPartialResults** - 2147745808 (0x80040010)
</dt> <dd>

Non tutti gli oggetti, gli enumeratori o gli aggiornamenti annidati sono stati aggiornati correttamente. Questo restituito non è un errore, ma un'indicazione che l'operazione è stata incompleta.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio di codice di script seguente viene illustrato come ottenere contatori delle prestazioni non elaborati e non elaborati per il processo di sistema. Gli oggetti vengono aggiornati ogni due secondi e le proprietà visualizzate.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

