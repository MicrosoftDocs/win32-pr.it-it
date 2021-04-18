---
description: L'API di scripting per WMI contiene flag, valori comuni e codici di errore.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Esecuzione di script di costanti API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309899"
---
# <a name="scripting-api-constants"></a>Esecuzione di script di costanti API

WMI usa diversi tipi di costanti nel parametro *iFlags* delle chiamate al metodo nell'API di [Scripting per WMI](scripting-api-for-wmi.md).

Visual Basic applicazioni possono includere la libreria dei tipi per l'API di scripting, wbemdisp. tlb. Gli script non sono in grado di accedere alle costanti nella libreria dei tipi, a meno che non utilizzino i <REFERENCE> tag o del <OBJECT> formato di file XML WSH (Windows script host), come descritto in [utilizzo della libreria dei tipi di scripting WMI](using-the-wmi-scripting-type-library.md). In caso contrario, uno script deve usare il valore della costante.

## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Definire i livelli di autenticazione di sicurezza.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Definire il modo in cui viene eseguita un'operazione di scrittura in una classe o in un'istanza.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Definire i tipi CIM validi di un valore della proprietà.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Definire le impostazioni per il confronto degli oggetti e usate da [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Definisce un flag di sicurezza usato come parametro nelle chiamate al metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) in caso di errore di una connessione a WMI in un computer remoto.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Definire gli errori che possono essere restituiti dall' [API di scripting per](scripting-api-for-wmi.md) le chiamate WMI.

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Definisce le costanti utilizzate da [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)e [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Definire i livelli di rappresentazione di sicurezza. Queste costanti vengono usate con [**SWbemSecurity**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Definire i formati di testo oggetto validi che devono essere usati da [**SWbemObjectEx. \_ gettext**](swbemobjectex-gettext-.md).

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Definire i privilegi. Queste costanti vengono usate con [**SWbemSecurity**](swbemsecurity.md) per concedere i privilegi necessari per alcune operazioni.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Definire la profondità dell'enumerazione o della query, che determina il numero di oggetti restituiti da una chiamata.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Definisce il contenuto del testo dell'oggetto generato e viene usato da [**SWbemObject. \_ GetObjectText**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Definisce le costanti di timeout. Questa costante viene utilizzata da [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).

</dd> </dl>

## <a name="combining-flags"></a>Combinazione di flag

È possibile combinare i flag per influenzare più di un aspetto della chiamata API.

Per creare, ad esempio, una chiamata [*semisincrono*](gloss-s.md) , il parametro *iFlags* in una chiamata [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md) deve contenere due flag: **WbemFlagReturnImmediately** e **WbemFlagForwardOnly**. Il valore di **WbemFlagReturnImmediately** è 16 e il valore di **WbemFlagForwardOnly** è 32. Poiché non è possibile accedere alle costanti in base al nome, i valori di questi flag vengono combinati, producendo un valore *iFlags* pari a 48.

Nell'esempio di script seguente viene illustrata la chiamata a.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Non tutti i flag possono essere combinati poiché molti si escludono a vicenda e possono produrre risultati imprevedibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



