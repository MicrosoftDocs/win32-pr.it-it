---
description: È possibile utilizzare i metodi di un oggetto SWbemServices per eseguire operazioni su uno spazio dei nomi in un host locale o in un host remoto. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Oggetto SWbemServices (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309773"
---
# <a name="swbemservices-object"></a>Oggetto SWbemServices

È possibile utilizzare i metodi di un oggetto **SWbemServices** per eseguire operazioni su uno spazio dei nomi in un host locale o in un host remoto. Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemServices** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemServices** dispone di questi metodi.



| Metodo                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Recupera le istanze di risorse gestite associate a una risorsa specificata tramite una o più classi di associazione. Si specifica il percorso dell'oggetto per l'endpoint di origine e [**AssociatorsOf**](swbemservices-associatorsof.md) restituisce le risorse gestite sull'endpoint opposto. Il metodo **AssociatorsOf** esegue la stessa funzione eseguita dalla query WQL "ASSOCIATORS of".<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | Restituisce in modo asincrono una raccolta di oggetti (classi o istanze) associati a un oggetto specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Delete**](swbemservices-delete.md)                                         | Elimina un'istanza di una risorsa gestita (o una definizione di classe dal repository CIM).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Elimina in modo asincrono la classe o l'istanza specificata nel percorso dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Fornisce un modo alternativo per eseguire un metodo definito da una definizione di classe di risorse gestite. Utilizzato principalmente nelle situazioni in cui il linguaggio di scripting non supporta i parametri out. Ad esempio, JScript non supporta parametri out.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Esegue in modo asincrono un metodo esportato da un provider di metodi.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Esegue una query di sottoscrizione di eventi per ricevere eventi. Una query di sottoscrizione di eventi è una query che definisce una modifica all'ambiente gestito che si desidera monitorare. Quando si verifica la modifica, l'infrastruttura WMI recapita un evento che descrive la modifica allo script chiamante.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Esegue in modo asincrono una query per ricevere eventi.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Esegue una query per recuperare una raccolta di istanze di risorse gestite da WMI (o definizioni di classe). [**ExecQuery**](swbemservices-execquery.md) può essere usato per recuperare una raccolta filtrata di istanze che soddisfano i criteri definiti nella query passata a **ExecQuery**.<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Esegue in modo asincrono una query per recuperare gli oggetti.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Recupero**](swbemservices-get.md)                                               | Recupera una singola istanza di una risorsa gestita (o definizione di classe) in base a un percorso dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | Recupera in modo asincrono un oggetto, ovvero una definizione di classe o un'istanza, in base al percorso dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Recupera tutte le istanze di una risorsa gestita in base al nome di una classe. Per impostazione predefinita, [**InstancesOf**](swbemservices-instancesof.md) esegue un recupero approfondito. Ovvero, **InstancesOf** recupera le istanze della risorsa identificata dal nome della classe passato al metodo e recupera anche tutte le istanze di tutte le risorse che sono sottoclassi (definite sotto) della classe di destinazione.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Restituisce in modo asincrono le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ReferencesTo**](swbemservices-referencesto.md)                             | Restituisce tutte le associazioni che fanno riferimento a una risorsa specificata. Il modo migliore per comprendere [**ReferencesTo**](swbemservices-referencesto.md) consiste nel confrontarlo con il metodo [**AssociatorsOf**](swbemservices-associatorsof.md) . **AssociatorsOf** restituisce le risorse dinamiche che si trovano all'estremità opposta di un'associazione. **ReferencesTo** restituisce l'associazione stessa. Il metodo **ReferencesTo** esegue la stessa funzione eseguita dalla query WQL "References of".<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Restituisce in modo asincrono una raccolta di tutte le classi di associazione o di istanze che fanno riferimento a una classe o a un'istanza specifica.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | Recupera tutte le sottoclassi di una classe specificata dal repository CIM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | Restituisce in modo asincrono una raccolta di sottoclassi per una classe specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemServices** dispone di queste proprietà.



| Proprietà                                                 | Tipo di accesso          | Descrizione                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Sicurezza\_**](swbemservices-security-.md)<br/> | Sola lettura<br/> | Utilizzato per ottenere o impostare le impostazioni di sicurezza per un oggetto **SWbemServices** .<br/> |



 

## <a name="remarks"></a>Commenti

I metodi possono essere chiamati in modalità sincrona, in modalità asincrona o in modalità semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

**Overview**

**SWbemServices** serve due ruoli primari. In primo luogo, l'oggetto **SWbemServices** rappresenta una connessione autenticata a uno spazio dei nomi WMI in un computer di destinazione. In secondo luogo, **SWbemServices** è l'oggetto di automazione utilizzato per recuperare le risorse gestite da WMI. È possibile ottenere un riferimento a un oggetto **SWbemServices** in uno dei due modi seguenti:

-   Come illustrato nella maggior parte degli script WMI presentati finora, è possibile utilizzare la funzione VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) in combinazione con il moniker WMI "winmgmts:". Nell'esempio seguente viene rappresentata la forma più semplice di una connessione WMI. Nell'esempio viene eseguita la connessione allo spazio dei nomi predefinito (in genere "root \\ CIMv2") nel computer locale:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   È anche possibile usare il metodo [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) dell'oggetto [**SWbemLocator**](swbemlocator.md) per ottenere un riferimento a un oggetto **SWbemServices** .

Dopo aver ottenuto un riferimento a un oggetto **SWbemServices** , usare il riferimento all'oggetto per chiamare 1 di 18 metodi disponibili usando **SWbemServices**. **SWbemServices** può restituire uno dei tre diversi oggetti della libreria di scripting WMI ([**SWbemObjectSet**](swbemobjectset.md), [**SWbemObject**](swbemobject.md)o [**SWbemEventSource**](swbemeventsource.md)), a seconda del metodo chiamato. Conoscere il tipo di oggetto restituito da ogni metodo consentirà di determinare il passaggio successivo che lo script deve eseguire. Se, ad esempio, si ottiene un **SWbemObjectSet**, è necessario enumerare la raccolta per accedere a ogni **SWbemObject** nella raccolta. Se si ottiene un **SWbemObject**, è possibile accedere immediatamente ai metodi e alle proprietà dell'oggetto senza prima enumerare la raccolta.

**Modalità di funzionamento**

**SWbemServices** supporta tre modalità di funzionamento: sincrona, asincrona e semisincrono.

-   **Sincrono**. In modalità sincrona, lo script blocca (sospende) fino al completamento del metodo **SWbemServices** . Non solo lo script è in attesa, ma nei casi in cui WMI recupera le istanze di risorse gestite, WMI compila l'intera [**SWbemObjectSet**](swbemobjectset.md) in memoria prima che il primo byte di dati venga restituito allo script chiamante. Ciò può influire negativamente sulle prestazioni dello script e sul computer in cui è in esecuzione lo script. Ad esempio, il recupero sincrono di migliaia di eventi dai registri eventi di Windows può richiedere molto tempo e usare una grande quantità di memoria. Per questi motivi, le operazioni sincrone non sono consigliate, ad eccezione dei tre metodi ([**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)e [**Get**](swbemservices-get.md)) sincroni per impostazione predefinita. Questi metodi non restituiscono set di dati di grandi dimensioni, pertanto l'operazione semisincrono non è obbligatoria.
-   **Asincrono**. In modalità asincrona lo script chiama uno dei nove metodi asincroni e restituisce immediatamente un risultato. Ovvero, non appena viene chiamato il metodo asincrono, lo script riprende a eseguire la riga di codice successiva. Per usare un metodo asincrono, lo script deve prima creare un oggetto [**SWbemSink**](swbemsink.md) e una subroutine speciale denominata gestore eventi. WMI esegue l'operazione asincrona e invia una notifica allo script chiamando la subroutine del gestore eventi al termine dell'operazione.
-   **Semisincrono**. La modalità semisincrono è un compromesso tra sincrono e asincrono. Le operazioni semisincrono offrono prestazioni migliori rispetto alle operazioni sincrone, ma non richiedono informazioni aggiuntive e passaggi di scripting necessari per gestire le operazioni asincrone. Si tratta del tipo di operazione predefinito per la maggior parte delle query WMI.

    In modalità semisincrono, lo script chiama uno dei sei metodi di recupero dei dati e restituisce immediatamente un risultato. WMI recupera le risorse gestite in background quando l'esecuzione dello script continua. Man mano che vengono recuperate, le risorse vengono immediatamente restituite allo script tramite un SWbemObjectSet. È possibile iniziare ad accedere alle risorse gestite senza attendere l'assemblaggio dell'intera raccolta.

    Quando si lavora con risorse gestite con molte istanze, ovvero con un valore maggiore di 1.000, si verificano le operazioni semisincrono, ad esempio [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) e [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). L'avvertenza è il risultato del modo in cui WMI gestisce le istanze di risorse gestite. Per ogni istanza di una risorsa gestita, WMI crea e memorizza nella cache un oggetto [**SWbemObject**](swbemobject.md) . Quando esiste un numero elevato di istanze per una risorsa gestita, il recupero delle istanze può monopolizzare le risorse disponibili, riducendo le prestazioni dello script e del computer.

    Per risolvere il problema, è possibile ottimizzare le chiamate al metodo semisincrono usando il flag **wbemFlagForwardOnly** . Il flag **wbemFlagForwardOnly** , combinato con il flag **wbemFlagReturnImmediately** (il flag semisincrono predefinito), indica a WMI di restituire un [**SWbemObjectSet**](swbemobjectset.md)di sola trasmissione, che elimina il problema di prestazioni del set di dati di grandi dimensioni. Tuttavia, l'uso del flag **wbemFlagForwardOnly** comporta un costo. Un **SWbemObjectSet** di sola trasmissione può essere enumerato una sola volta. Una volta eseguito l'accesso a ogni [**SWbemObject**](swbemobject.md) in un **SWbemObjectSet** di sola trasmissione, viene rilasciata la memoria allocata all'istanza.

Fatta eccezione per i metodi asincroni [**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md), [**Get**](swbemservices-get.md)e Nine, semisincrono è la modalità di funzionamento predefinita e consigliata.

**Metodi di uso comune**

I metodi usati più spesso negli script di amministrazione del sistema sono [**InstancesOf**](swbemservices-instancesof.md), [**ExecQuery**](swbemservices-execquery.md), [**Get**](swbemservices-get.md)e [**ExecNotificationQuery**](swbemservices-execnotificationquery.md). Anche se spesso usato, **InstancesOf** non è necessariamente il metodo consigliato per recuperare informazioni (anche se è probabilmente il modo più semplice).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

