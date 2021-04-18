---
description: Il provider SNMP supporta la scrittura nei file di log e nel debugger.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309881"
---
# <a name="snmp-events"></a>Eventi SNMP

Il provider SNMP supporta la scrittura nei file di log e nel debugger.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Un numero di chiavi e valori del registro di sistema definisce il livello e il tipo di registrazione attualmente in corso di generazione:

-   Debug

    La chiave del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Registration** contiene il valore di registrazione che indica se è possibile scrivere le informazioni nel debugger. Il valore di registrazione è impostato su 0 per disabilitare l'output del debug o 1 per abilitarlo. La registrazione è un \_ valore reg DWORD.

-   Registrazione

    La chiave del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging \\ WBEMSNMP** include tutte le informazioni di registrazione specifiche per il provider SNMP. Nella tabella seguente sono elencati i valori associati a questa chiave.



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
<td><strong>REG_DWORD</strong><br/> Accetta valori integer compresi tra 1024 e 2 ^ 32-1. Il valore corrisponde alla dimensione massima consentita, in byte, per il file di log. Se è minore di 1024, il meccanismo di registrazione utilizza un valore pari a 1024. Per questo valore è consigliata una dimensione minima di 8 KB. Quando il file raggiunge le dimensioni specificate da MaxFileSize, il nome del file viene anteposto a un carattere ' ~' e viene creato un nuovo file. Pertanto, lo spazio massimo su disco necessario per la registrazione è due volte questo valore.<br/></td>
</tr>
<tr class="odd">
<td>File</td>
<td><strong>REG_SZ</strong><br/> Definisce il nome del file a cui viene inviato l'output di debug quando il tipo di registrazione è impostato su "file". Il valore predefinito è " <WBEMLOGS> \wbemsnmp.log." Se la <WBEMLOGS> Directory non può essere determinata dalla sezione del registro di sistema WMI, il valore predefinito è' c:\wbemsnmp.log '. Se viene utilizzata una condivisione, ad esempio \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log dove M: è \\ machine\share, l'account di sistema locale in cui è in esecuzione WMI deve disporre dei diritti di accesso in lettura/scrittura al \\ machine\share.<br/></td>
</tr>
<tr class="even">
<td>Level</td>
<td><strong>REG_DWORD</strong><br/> Accetta valori integer compresi tra 0 e 2 ^ 32-1. Il valore è una maschera logica costituita da 32 bit. Le seguenti maschere di bit vengono combinate per definire il tipo di output di debug generato:<br/>
<ul>
<li>0: chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP</li>
<li>1: implementazione del provider di classi SNMP</li>
<li>2: chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di istanze SNMP</li>
<li>3: implementazione del provider di istanze SNMP</li>
<li>4: libreria di classi SNMP</li>
<li>5: SNMP ARCHIVIO SMIR</li>
<li>6: correlatore SNMP</li>
<li>7: codice di mapping dei tipi SNMP</li>
<li>8: codice di threading SNMP</li>
<li>9: implementazione e interfacce del provider di eventi SNMP</li>
</ul>
Impostare level su (2 ^ 0 + 2 ^ 8 =) 257 per le operazioni che interessano le chiamate ai metodi <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP e operazioni utilizzando il codice di threading SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




