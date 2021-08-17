---
description: Definisce un provider e i contatori forniti.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Tipo complesso provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4470754e710faf9f7abe5a94cfb2e08e6e79c1b0415110b96dbac35807556911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061068"
---
# <a name="provider-complex-type"></a>Tipo complesso provider

Definisce un provider e i contatori forniti.

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento        | Tipo                                                                   | Descrizione                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Counterset** | [**man:counterSet**](performance-counters-counterset-complex-type.md) | Identifica l'insieme di contatori che contiene uno o più contatori correlati logicamente.<br/> |



## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Applicationidentity</td>
<td><strong>xs:string</strong></td>
<td>Nome del file binario che contiene le stringhe di risorse localizzate, un file .exe o .dll (non includere il percorso del file binario).<br/> LLodctr.exe utilità usa il percorso del parametro facoltativo [<em>path</em>] per cercare il file binario. Ad esempio, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>percorso</em>]]. Se non si include il parametro [<em>path</em>], Lodctr.exe cerca nella cartella che contiene il manifesto.<br/></td>
</tr>
<tr class="even">
<td>callback</td>

<td>Questo attributo indica che si desidera ricevere una notifica quando un consumer esegue determinate azioni. <br/> Se si include questo attributo, lo strumento CTRPP usa la firma della funzione <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> alternativa, che consente di passare il nome della funzione che implementa la funzione di callback <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a><br/> In alternativa alla specifica di questo attributo, è possibile usare l'argomento<a href="ctrpp.md">CTRPP</a> <strong>-NotificationCallback.</strong><br/> <strong>Windows Vista:</strong> L'unico valore valido per questo attributo è &quot; &quot; personalizzato. <a href="ctrpp.md">L'utilità CTRPP</a> genera il modello per una funzione di callback <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a> Il modello è incluso nel file CTRPP generato da CTRPP. <br/> <br/></td>
</tr>
<tr class="odd">
<td>guida provider</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></td>
<td>GUID stringa che identifica in modo univoco il provider nel manifesto. Il GUID deve essere univoco all'interno del manifesto.<br/> È necessario specificare un nuovo GUID solo quando viene modificata la versione dell'applicazione (se si supportano installazioni side-by-side).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Nome utilizzato per creare il nome della Win32_PerfRawData WMI. Se non si specifica un nome, &quot; counters &quot; viene utilizzato come nome della classe.<br/></td>
</tr>
<tr class="odd">
<td>Providertype</td>

<td>Identifica se il provider è un provider in modalità utente, un provider in modalità kernel o un provider di driver. I valori possibili sono i seguenti.<br/> 
<table>
<thead>
<tr class="header">
<th>Termine</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Usermode<br/></td>
<td>Specificare questa modalità per un componente in modalità utente, ad esempio un'applicazione, una DLL o un driver in modalità utente. Le estensioni tipiche per i componenti in modalità utente sono .exe o .dll. Questo è il valore predefinito.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>Kernel<br/></td>
<td>Specificare questa modalità per un componente in modalità kernel, ad esempio un driver WDM o WDF. L'estensione tipica per i componenti in modalità kernel è .sys.<br/> <strong>Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato fino Windows 7 e Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td><p>Definisce il valore iniziale dell'indice delle risorse <a href="ctrpp.md">utilizzato da CTRPP</a> per generare gli identificatori di risorsa.</p></td>
</tr>
<tr class="odd">
<td>simbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td><p>Nome simbolico che identifica il provider. Lo <a href="ctrpp.md">strumento CTRPP</a> crea una variabile HANDLE che è possibile usare quando si chiamano funzioni che richiedono un handle per il provider ( ad <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>esempio, PerfSetULongCounterValue</strong></a>). Il nome simbolico è il nome della variabile.</p>
<p>Se si include <strong>l'argomento -prefix</strong> quando si chiama <a href="ctrpp.md">CTRPP,</a>la stringa di prefisso viene aggiunta all'inizio del nome simbolico.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




