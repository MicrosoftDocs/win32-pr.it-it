---
description: Concettualmente simile a un Uniform Resource Locator (URL), il percorso di un oggetto WMI è una stringa che identifica in modo univoco lo spazio dei nomi in un server, una classe all'interno di uno spazio dei nomi o istanze di una classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Descrizione della posizione di un oggetto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310375"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Descrizione della posizione di un oggetto WMI

Concettualmente simile a un Uniform Resource Locator (URL), il percorso di un oggetto WMI è una stringa che identifica in modo univoco lo spazio dei nomi in un server, una classe all'interno di uno spazio dei nomi o istanze di una classe. Il percorso di un oggetto è gerarchico e contiene diversi elementi che descrivono la posizione dell'oggetto in questione. Come i percorsi di file, i percorsi degli oggetti WMI possono essere descritti in modo completo o specificato come percorso relativo.

Lo spazio dei nomi di un oggetto WMI è elencato nella pagina di riferimento di WMI. Ad esempio, il percorso della maggior parte delle classi supportate dai [provider WMI cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) si trova nello \\ \\ spazio dei nomi CIMV2 radice. Il codice di PowerShell seguente descrive una chiamata per recuperare l'oggetto [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) nel computer locale:

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

In alternativa, un'istanza specifica di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) può avere il percorso seguente dalla proprietà [**SWbemObject. Path \_**](swbemobject-path-.md) .

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

Nell'esempio seguente viene illustrato il percorso relativo di questa istanza, come visualizzato visualizzando la proprietà [**RelPath**](swbemobjectpath-relpath.md) dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) restituito dalla chiamata a [**SWbemObject. Path \_**](swbemobject-path-.md).

`Win32_LogicalDisk.DeviceID="A:"`

Si noti che **DeviceID** è la proprietà chiave della [**classe \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

## <a name="c"></a>C++

Nella tabella seguente sono elencati i tipi di percorso degli oggetti e i metodi associati che richiedono percorsi di oggetti.



<table>
<thead>
<tr class="header">
<th>Tipo di percorso dell'oggetto</th>
<th>Metodo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Classe</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a><br />
[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Classe</a> o <a href="describing-an-instance-object-path.md">istanza</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a><br />
[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Istanza</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a><br />
[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Script

I percorsi degli oggetti possono essere costruiti in diversi modi:

-   Recuperare la proprietà di un metodo che restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) .
-   Recuperare la proprietà [**SWbemObject. \_ path**](swbemobject-path-.md) .
-   Creare una variabile di stringa che contiene il percorso dell'oggetto.

Nella tabella seguente sono elencati gli oggetti di scripting che richiedono percorsi di oggetti.



<table>
<thead>
<tr class="header">
<th>Oggetto di scripting</th>
<th>Metodo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a><br />
[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)<br />
[<strong>Elimina</strong>] (swbemservices-delete.md)<br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)<br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)<br />
[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)<br />
[<strong>Get</strong>] (swbemservices-get.md)<br />
[<strong>GetAsync</strong>] (swbemservices-getasync.md)<br />
[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md)<br />
[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Elemento</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
