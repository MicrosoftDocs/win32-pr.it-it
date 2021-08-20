---
description: Il provider SNMP supporta la scrittura nei file di log e nel debugger.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925ce6bb5eca0a3c067470255296ba6c9f66c0183b2b74aa6cfa4a25824446d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816647"
---
# <a name="snmp-events"></a>Eventi SNMP

Il provider SNMP supporta la scrittura nei file di log e nel debugger.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Diversi valori e chiavi del Registro di sistema definiscono il livello e il tipo di registrazione attualmente generati:

-   Debug

    La **chiave del Registro di sistema \_ HKEY LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM \\ PROVIDERS \\ LOGGING** contiene il valore di registrazione che indica se è possibile scrivere informazioni nel debugger. Il valore di registrazione è impostato su 0 per disabilitare l'output di debug o su 1 per abilitarlo. La registrazione è un valore \_ DWORD REG.

-   Registrazione

    La chiave del Registro di **sistema HKEY \_ LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM \\ PROVIDERS LOGGING \\ \\ WBEMSNMP** contiene tutte le informazioni di registrazione specifiche del provider SNMP. Nella tabella seguente sono elencati i valori associati a questa chiave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>REG_SZ</strong><br/> Accetta uno dei valori seguenti:<br/> &quot;File &quot; = (impostazione predefinita) Invia l'output di debug a un file.<br/> &quot;Debugger &quot; = Invia l'output di debug al debugger.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Accetta valori interi da 1024 a 2^32-1. Il valore è la dimensione massima consentita in byte per il file di log. Se è minore di 1024, il meccanismo di registrazione usa il valore 1024. Per questo valore è consigliabile una dimensione minima di 8 KB. Quando il file raggiunge le dimensioni specificate da MaxFileSize, al nome del file viene anteposto un carattere "~" e viene creato un nuovo file. Di conseguenza, lo spazio massimo su disco necessario per la registrazione è il doppio di questo valore.<br/></td>
</tr>
<tr class="odd">
<td>File</td>
<td><strong>REG_SZ</strong><br/> Definisce il nome del file a cui viene inviato l'output di debug quando il tipo di registrazione è impostato su 'File'. Il valore predefinito è <WBEMLOGS> '\wbemsnmp.log'. Se non è possibile determinare la directory dalla sezione del Registro di sistema WMI, il valore predefinito <WBEMLOGS> è 'c:\wbemsnmp.log'. Se si usa una condivisione, ad esempio \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log dove M: è machine\share, l'account SYSTEM locale in cui viene eseguito WMI deve disporre dei diritti di accesso in \\ lettura/scrittura al \\ computer\share.<br/></td>
</tr>
<tr class="even">
<td>Level</td>
<td><strong>REG_DWORD</strong><br/> Accetta valori interi da 0 a 2^32-1. Il valore è una maschera logica costituita da 32 bit. Le maschere di bit seguenti vengono combinate per definire il tipo di output di debug generato:<br/>
<ul>
<li>0: Chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP</li>
<li>1: Implementazione del provider di classi SNMP</li>
<li>2: Chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di istanze SNMP</li>
<li>3: Implementazione del provider di istanze SNMP</li>
<li>4: Libreria di classi SNMP</li>
<li>5: SNMP SMIR</li>
<li>6: Correlatore SNMP</li>
<li>7: Codice di mapping dei tipi SNMP</li>
<li>8: Codice di threading SNMP</li>
<li>9: Implementazione e interfacce del provider di eventi SNMP</li>
</ul>
Impostare Level su (2^0 + 2^8=) 257 per le operazioni che coinvolgono chiamate ai metodi <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP e le operazioni che usano il codice di threading SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




