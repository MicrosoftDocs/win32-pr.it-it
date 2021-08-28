---
description: L'API scripting per WMI contiene flag, valori comuni e codici di errore.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Costanti dell'API di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ebbfbc1061d8bca03f52dd8cb7583fbe23ebb33a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885248"
---
# <a name="scripting-api-constants"></a>Costanti dell'API di scripting

WMI usa diversi tipi di costanti nel parametro *iflags* delle chiamate al metodo [nell'API scripting per WMI](scripting-api-for-wmi.md).

Visual Basic applicazioni possono includere la libreria dei tipi per l'API di scripting Wbemdisp.tlb. Gli script non possono accedere alle costanti nella libreria dei tipi a meno che non usino i tag REFERENCE o OBJECT dal &lt; formato di file XML &gt; &lt; &gt; WSH (Windows Script Host), [](using-the-wmi-scripting-type-library.md)come descritto in Uso della libreria dei tipi di scripting WMI . In caso contrario, uno script deve usare il valore della costante .

## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Definire i livelli di autenticazione di sicurezza.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Definire la modalità di esecuzione di un'operazione di scrittura in una classe o in un'istanza di .

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Definire i tipi CIM validi di un valore di proprietà.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Definire le impostazioni per il confronto tra oggetti e vengono usate da [**SWbemObject.CompareTo \_**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Definisce un flag di sicurezza utilizzato come parametro nelle chiamate al metodo [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) quando si verifica un errore di connessione a WMI in un computer remoto.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Definire gli errori che possono essere restituiti [dall'API di scripting per le chiamate WMI.](scripting-api-for-wmi.md)

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Definisce le costanti usate da [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)e [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Definire i livelli di rappresentazione di sicurezza. Queste costanti vengono usate con [**SWbemSecurity**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Definire i formati di testo degli oggetti validi che devono essere usati da [**SWbemObjectEx.GetText \_**](swbemobjectex-gettext-.md).

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

Definisce il contenuto del testo dell'oggetto generato e viene usato da [**SWbemObject.GetObjectText \_**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Definisce le costanti di timeout. Questa costante viene usata [**da SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).

</dd> </dl>

## <a name="combining-flags"></a>Combinazione di flag

È possibile combinare flag per influire su più aspetti della chiamata API.

Ad esempio, per creare una chiamata [*semisincronous,*](gloss-s.md) il parametro *iFlags* in una chiamata [**cQuery \_SWbemServices.Exe**](swbemservices-execquery.md) deve contenere due flag: **WbemFlagReturnImmediately** e **WbemFlagForwardOnly**. Il valore di **WbemFlagReturnImmediately** è 16 e il valore di **WbemFlagForwardOnly** è 32. Poiché non è possibile accedere alle costanti in base al nome, i valori di questi flag vengono combinati, producendo un *valore iFlags* pari a 48.

Nell'esempio di script seguente viene illustrata la chiamata .


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Non tutti i flag possono essere combinati perché molti si escludono a vicenda e possono produrre risultati imprevedibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



