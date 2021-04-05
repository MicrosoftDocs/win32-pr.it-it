---
description: Definisce un provider e i contatori che fornisce.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Tipo complesso provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881741"
---
# <a name="provider-complex-type"></a><span data-ttu-id="9bff5-103">Tipo complesso provider</span><span class="sxs-lookup"><span data-stu-id="9bff5-103">provider Complex Type</span></span>

<span data-ttu-id="9bff5-104">Definisce un provider e i contatori che fornisce.</span><span class="sxs-lookup"><span data-stu-id="9bff5-104">Defines a provider and the counters that it provides.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="9bff5-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9bff5-105">Child elements</span></span>



| <span data-ttu-id="9bff5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9bff5-106">Element</span></span>        | <span data-ttu-id="9bff5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bff5-107">Type</span></span>                                                                   | <span data-ttu-id="9bff5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bff5-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bff5-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="9bff5-109">**counterSet**</span></span> | [<span data-ttu-id="9bff5-110">**uomo: contatore**</span><span class="sxs-lookup"><span data-stu-id="9bff5-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="9bff5-111">Identifica l'insieme di contatori che contiene uno o più contatori correlati logicamente.</span><span class="sxs-lookup"><span data-stu-id="9bff5-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="9bff5-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="9bff5-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9bff5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="9bff5-113">Name</span></span></th>
<th><span data-ttu-id="9bff5-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bff5-114">Type</span></span></th>
<th><span data-ttu-id="9bff5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bff5-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bff5-116">applicationIdentity</span><span class="sxs-lookup"><span data-stu-id="9bff5-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="9bff5-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="9bff5-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="9bff5-118">Nome del file binario che contiene le stringhe di risorsa localizzate, ovvero un file con estensione exe o dll (non includere il percorso del file binario).</span><span class="sxs-lookup"><span data-stu-id="9bff5-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="9bff5-119">L'utilità Lodctr.exe usa il percorso dal parametro facoltativo [<em>path</em>] per cercare il file binario.</span><span class="sxs-lookup"><span data-stu-id="9bff5-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="9bff5-120">Ad esempio, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span><span class="sxs-lookup"><span data-stu-id="9bff5-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="9bff5-121">Se non si include il parametro [<em>path</em>], Lodctr.exe Cerca nella cartella che contiene il manifesto.</span><span class="sxs-lookup"><span data-stu-id="9bff5-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bff5-122">callback</span><span class="sxs-lookup"><span data-stu-id="9bff5-122">callback</span></span></td>

<td><span data-ttu-id="9bff5-123">Questo attributo indica che si desidera ricevere una notifica quando un consumer esegue determinate azioni.</span><span class="sxs-lookup"><span data-stu-id="9bff5-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="9bff5-124">Se si include questo attributo, lo strumento CTRPP usa la firma della funzione <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> alternativa, che viene usata per passare il nome della funzione che implementa la funzione di callback <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9bff5-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="9bff5-125">In alternativa alla specifica di questo attributo, è possibile usare l'argomento <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> .</span><span class="sxs-lookup"><span data-stu-id="9bff5-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="9bff5-126"><strong>Windows Vista:</strong> L'unico valore valido per questo attributo è &quot; Custom &quot; .</span><span class="sxs-lookup"><span data-stu-id="9bff5-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="9bff5-127">L'utilità <a href="ctrpp.md">CTRPP</a> genera il modello per una funzione di callback <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9bff5-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="9bff5-128">Il modello è incluso nel file con estensione c generato da CTRPP.</span><span class="sxs-lookup"><span data-stu-id="9bff5-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bff5-129">providerGuid</span><span class="sxs-lookup"><span data-stu-id="9bff5-129">providerGuid</span></span></td>
<td><span data-ttu-id="9bff5-130"><a href="performance-counters-guidtype-simple-type.md"><strong>uomo: GUIDType</strong></a></span><span class="sxs-lookup"><span data-stu-id="9bff5-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="9bff5-131">GUID di stringa che identifica in modo univoco il provider nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="9bff5-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="9bff5-132">Il GUID deve essere univoco all'interno del manifesto.</span><span class="sxs-lookup"><span data-stu-id="9bff5-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="9bff5-133">È necessario fornire un nuovo GUID solo quando cambia la versione dell'applicazione (se si supportano installazioni affiancate).</span><span class="sxs-lookup"><span data-stu-id="9bff5-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bff5-134">providerName</span><span class="sxs-lookup"><span data-stu-id="9bff5-134">providerName</span></span></td>
<td><span data-ttu-id="9bff5-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="9bff5-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="9bff5-136">Nome utilizzato per creare il nome della classe WMI Win32_PerfRawData.</span><span class="sxs-lookup"><span data-stu-id="9bff5-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="9bff5-137">Se non si specifica un nome, i &quot; contatori &quot; vengono usati come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="9bff5-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bff5-138">providerType</span><span class="sxs-lookup"><span data-stu-id="9bff5-138">providerType</span></span></td>

<td><span data-ttu-id="9bff5-139">Indica se il provider è un provider in modalità utente, un provider in modalità kernel o un provider di driver.</span><span class="sxs-lookup"><span data-stu-id="9bff5-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="9bff5-140">I valori possibili sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bff5-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9bff5-141">Termine</span><span class="sxs-lookup"><span data-stu-id="9bff5-141">Term</span></span></th>
<th><span data-ttu-id="9bff5-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bff5-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bff5-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span><span class="sxs-lookup"><span data-stu-id="9bff5-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="9bff5-144">Specificare questa modalità per un componente in modalità utente, ad esempio un'applicazione, una DLL o un driver in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="9bff5-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="9bff5-145">Le estensioni tipiche per i componenti in modalità utente sono exe o dll.</span><span class="sxs-lookup"><span data-stu-id="9bff5-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="9bff5-146">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bff5-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bff5-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span><span class="sxs-lookup"><span data-stu-id="9bff5-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="9bff5-148">Specificare questa modalità per un componente in modalità kernel, ad esempio un driver WDM o CDR.</span><span class="sxs-lookup"><span data-stu-id="9bff5-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="9bff5-149">L'estensione tipica per i componenti in modalità kernel è. sys.</span><span class="sxs-lookup"><span data-stu-id="9bff5-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="9bff5-150"><strong>Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato fino a Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="9bff5-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bff5-151">resourceBase</span><span class="sxs-lookup"><span data-stu-id="9bff5-151">resourceBase</span></span></td>
<td><span data-ttu-id="9bff5-152"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="9bff5-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="9bff5-153">Definisce il valore di indice della risorsa iniziale utilizzato da <a href="ctrpp.md">CTRPP</a> per generare gli identificatori di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9bff5-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bff5-154">simbolo</span><span class="sxs-lookup"><span data-stu-id="9bff5-154">symbol</span></span></td>
<td><span data-ttu-id="9bff5-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="9bff5-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="9bff5-156">Nome simbolico che identifica il provider.</span><span class="sxs-lookup"><span data-stu-id="9bff5-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="9bff5-157">Lo strumento <a href="ctrpp.md">CTRPP</a> crea una variabile handle che è possibile usare quando si chiamano funzioni che richiedono un handle per il provider (ad esempio, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="9bff5-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="9bff5-158">Il nome simbolico è il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="9bff5-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="9bff5-159">Se si include l'argomento <strong>-Prefix</strong> quando si chiama <a href="ctrpp.md">CTRPP</a>, la stringa di prefisso viene aggiunta all'inizio del nome simbolico.</span><span class="sxs-lookup"><span data-stu-id="9bff5-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="9bff5-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bff5-160">Requirements</span></span>



| <span data-ttu-id="9bff5-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bff5-161">Requirement</span></span> | <span data-ttu-id="9bff5-162">Valore</span><span class="sxs-lookup"><span data-stu-id="9bff5-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9bff5-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bff5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9bff5-164">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bff5-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9bff5-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bff5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9bff5-166">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9bff5-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




