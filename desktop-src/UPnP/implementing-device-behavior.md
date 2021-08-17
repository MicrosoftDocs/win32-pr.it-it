---
title: Implementazione del comportamento del dispositivo
description: Il comportamento di un dispositivo è definito dai servizi esposti.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce2857c11a02ef5eeebe7b2cd5e75ee76138929e5bd95a2e3bdfa7ffd2c71dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137264"
---
# <a name="implementing-device-behavior"></a>Implementazione del comportamento del dispositivo

Il comportamento di un dispositivo è definito dai servizi esposti. Ogni servizio dispone di una descrizione del servizio che elenca le azioni e le variabili di stato. Nel loro insieme, queste descrizioni del servizio costituiscono l'interfaccia del servizio, che definisce il modo in cui un punto di controllo può interagire con un servizio. Ogni servizio deve avere almeno un'azione.

Per implementare un servizio, un dispositivo ospitato deve fornire un oggetto Component Object Model (COM) che espone l'interfaccia per il servizio. Nella descrizione del servizio le interfacce del servizio sono specificate in UPnP Template Language (UTL); Tuttavia, le interfacce degli oggetti COM vengono in genere specificate nel linguaggio IDL (Interface Definition Language). È anche possibile specificare l'interfaccia COM in una libreria dei tipi o in un file di intestazione. Platform Software Development Kit (SDK) include lo strumento Utl2idl, che converte una descrizione del servizio in UTL in un'interfaccia COM in IDL.

Gli esempi seguenti illustrano questo processo di conversione. La descrizione del servizio viene fornita dallo sviluppatore del dispositivo ed è scritta in UTL.

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

Il passaggio successivo consiste nell'eseguire lo strumento Utl2idl. Produce il file IDL che contiene l'interfaccia COM. Per altre informazioni sui file IDL e sulla parola chiave **interface,** vedere [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) (File e interfaccia di definizione dell'interfaccia) in MIDL reference (Informazioni di riferimento su MIDL).

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> Il valore restituito è il primo parametro out nell'elenco di argomenti nella descrizione del servizio, ma viene elencato come \[ ultimo parametro dopo la \] conversione.
> 
> Tutti gli altri parametri rimangono nello stesso ordine.

 

Per fornire la funzionalità del servizio, implementare questa interfaccia COM.

## <a name="obtaining-information-about-an-endpoint"></a>Recupero di informazioni su un endpoint

Nel framework UPnP le informazioni sull'endpoint includono informazioni su una richiesta e la relativa origine. Un dispositivo può esaminare queste informazioni per prendere una decisione sulla richiesta.

Le informazioni sull'endpoint sono facoltativamente disponibili per il servizio implementato. L'host del dispositivo ha accesso alle informazioni sull'endpoint. Tuttavia, l'host del dispositivo non comunica le informazioni al servizio implementato per impostazione predefinita. È possibile abilitare l'host del dispositivo per condividere le informazioni sull'endpoint con il servizio implementato modificando l'interfaccia COM nel file IDL (prodotto dallo strumento Utl2idl). È possibile aggiungere un \[ parametro in a ogni metodo che richiede informazioni \] sull'endpoint. L'elemento aggiuntivo nel parametro deve essere il primo nell'elenco di argomenti, un puntatore \[ a \] [**un'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e denominato in modo esplicito **namedremoteEndpointInfo.** Le modifiche al codice XML del servizio non sono obbligatorie o consigliate. L'esempio seguente illustra la nuova definizione del metodo **PowerOn** quando viene modificato in modo che riceva le informazioni sull'endpoint:

"HRESULT PowerOn( \[ in \] IUnknown \* remotingRemoteEndpointInfo);"

Un puntatore a un oggetto informazioni sull'endpoint, [**un'interfaccia IUPnPRemoteEndpointInfo,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) viene passato tramite questo nuovo parametro dall'host del dispositivo. **L'interfaccia IUPnPRemoteEndpointInfo** fornisce tre metodi per accedere alle informazioni sull'endpoint. È necessario chiamare il metodo appropriato per ottenere le informazioni sull'endpoint richieste dall'implementazione del servizio.

In alternativa alla modifica manuale dell'interfaccia COM, è possibile usare lo strumento Utl2idl con **l'opzione -ci.** Questa opzione fa sì che lo strumento abiliti il parametro delle informazioni sull'endpoint a ognuno dei metodi nell'interfaccia COM. **L'uso dell'opzione -ci** non facilita la modifica dei singoli metodi. Se le informazioni sull'endpoint non sono necessarie per tutti i metodi di un'interfaccia, è necessario aggiungere manualmente il parametro per produrre le implementazioni più efficienti.

## <a name="implementing-a-service-object"></a>Implementazione di un oggetto servizio

È necessario usare lo strumento Utl2idl per tradurre ogni descrizione del servizio di un dispositivo.

Un oggetto che fornisce la funzionalità per un servizio viene definito oggetto [*servizio*](s-gly.md). Oltre a fornire funzionalità del servizio, gli oggetti servizio gestiscono gli errori tramite [**l'interfaccia IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Per altre informazioni, vedere [Using the Device Host API with UPnP Technology (Uso dell'API host dei dispositivi con la tecnologia UPnP).](using-the-device-host-api-with-upnp-technology.md)

Per garantire la compatibilità con Visual Basic, che non supporta i parametri out, i parametri direction out /direction nella descrizione del servizio vengono convertiti in parametri \[ \] in out in  \[ \] IDL. Il server deve liberare questi \[ parametri in, \] out.

## <a name="implementing-a-device-control-object"></a>Implementazione di un oggetto controllo dispositivo

Oltre a implementare oggetti servizio, è necessario implementare un oggetto [*controllo dispositivo*](d-gly.md). Un oggetto controllo dispositivo è il punto centrale di gestione e controllo per gli oggetti servizio del dispositivo. Al momento della registrazione, l'oggetto controllo dispositivo viene passato all'host del dispositivo. Quando arriva una sottoscrizione di eventi o una richiesta di controllo per uno dei servizi del dispositivo, l'host del dispositivo chiama questo oggetto controllo dispositivo per ottenere l'oggetto servizio pertinente. A quel punto, l'oggetto controllo dispositivo crea un'istanza dell'oggetto servizio o restituisce l'interfaccia di un'istanza esistente dell'oggetto servizio.

È possibile registrare una descrizione del dispositivo in più computer o più volte nello stesso computer. Poiché il nome UDN (Unique Device Name) deve essere diverso per ogni istanza del dispositivo, l'host del dispositivo genera una rete definita dall'utente univoca per ogni dispositivo e dispositivo incorporato ogni volta che il dispositivo viene registrato. Usare la rete definita dall'utente specificata nel modello di descrizione del dispositivo per ottenere la rete definita dall'utente effettiva generata dall'host del dispositivo e associata al dispositivo. Per annullare la registrazione di un dispositivo, è necessario usare l'ID fornito dal framework UPnP quando il dispositivo è stato registrato.

Gli oggetti controllo dispositivo devono implementare [**l'interfaccia IUPnPDeviceControl.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) L'host del dispositivo richiama il metodo [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo dispositivo, passando la descrizione del dispositivo basata su UPnP pubblicata in precedenza per il dispositivo e una stringa di inizializzazione specificata al momento della registrazione (vedere Registrazione di un dispositivo ospitato con [l'host del dispositivo).](registering-a-hosted-device-with-the-device-host.md) Da questa descrizione del dispositivo, l'oggetto controllo dispositivo legge i nomi definiti dall'utente assegnati a ognuno dei dispositivi nell'albero dei dispositivi. È anche possibile usare il [**metodo IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) per ottenere queste informazioni.

Quando l'host del dispositivo richiede un puntatore a un oggetto servizio che implementa un particolare servizio, richiama il metodo [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) sull'oggetto controllo dispositivo. L'host del dispositivo passa la rete definita dall'utente e l'ID servizio del servizio per cui richiede un oggetto servizio e l'indirizzo di un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in corrispondenza del quale si prevede che il metodo restituirà un puntatore all'oggetto servizio. Il parametro UDN è necessario perché l'oggetto controllo dispositivo gestisce i servizi per l'intero albero dei dispositivi, inclusi i dispositivi annidati. Se l'host del dispositivo richiede un dispositivo annidato, **GetServiceObject** usa la rete definita dall'utente per identificarlo.

 

 