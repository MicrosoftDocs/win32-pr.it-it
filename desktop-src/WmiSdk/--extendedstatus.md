---
description: Utilizzato per segnalare informazioni dettagliate sullo stato e sull'errore.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319314"
---
# <a name="__extendedstatus-class"></a>\_\_Classe ExtendedStatus

La classe di sistema **\_ \_ ExtendedStatus** viene utilizzata per segnalare informazioni dettagliate sullo stato e sull'errore.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ExtendedStatus** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ExtendedStatus** dispone di queste proprietà.

<dl> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.

</dd> <dt>

**Operazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Operazione che viene eseguita al momento di un errore o di un'anomalia. In genere, Strumentazione gestione Windows (WMI) imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Parametri che coinvolgono un errore o una modifica dello stato. Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il provider che causa o segnala un errore o una modifica dello stato. Se un provider non è necessario, questa stringa è impostata su "Windows Management".

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un codice di errore o informazioni per un'operazione. Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo. Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ ExtendedStatus** è derivata dalla classe [**\_ \_ NotifyStatus**](--notifystatus.md) .

Usare la classe **\_ \_ ExtendedStatus** per segnalare informazioni più complesse rispetto a un semplice codice di risultato. I provider possono derivare le proprie classi da **\_ \_ ExtendedStatus** se richiedono più proprietà per descrivere gli errori.

La proprietà **statusCode** , ereditata dalla classe padre [**\_ \_ NotifyStatus**](--notifystatus.md) , è un Unsigned Integer che rappresenta il valore di errore o di stato. Quando le istanze di questa classe vengono restituite da un metodo da un provider dinamico, le proprietà **statusCode** e **Description** vengono impostate dal provider e le altre proprietà vengono impostate da WMI.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente, tratto da [FND: How to handle Configuration Manager asincrono Errors Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example in TechNet Gallery, descrive l'uso di **\_ \_ ExtendedStatus** per recuperare le informazioni sugli errori.


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

