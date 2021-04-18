---
title: Impostazioni predefinite .NET Framework
description: .NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300636"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo

## <a name="platforms"></a>Piattaforme

**Client**   di   Windows 8  
**Server**   di   Windows Server 2012  

## <a name="description"></a>Descrizione

.NET Framework 4,5 è abilitato per impostazione predefinita in Windows 8. Windows 8 non include .NET 3,5 per impostazione predefinita, ma i file per .NET 3,5 sono disponibili nel supporto di installazione di Windows 8 come funzionalità facoltativa.

Se l'utente sta eseguendo l'aggiornamento da Windows 7 a Windows 8, .NET Framework 3,5 è completamente abilitato per assicurarsi che tutte le app nel computer continuino a funzionare correttamente.

## <a name="manifestation"></a>Manifestazione

Se l'utente esegue un'installazione pulita di Windows 8, quindi installa app che richiedono .NET Framework 3,5 (o 2,0), attiverà una richiesta per i file .NET 3,5 necessari. In genere i file mancanti verranno scaricati da Windows Update (dopo aver chiesto all'utente l'autorizzazione), ma se non è possibile accedere a Windows Update, l'abilitazione di .NET Framework 3,5 avrà esito negativo a meno che non sia stata specificata un'origine alternativa per i file mancanti.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per abilitare .NET Framework 3,5 solo nei computer di test con installazioni pulite di Windows 8:

1.  Copiare \\ \\ le origini SxS \\ dall'immagine ISO di compilazione del sistema operativo montata in dotnet35 o in una cartella simile. Ad esempio:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Eseguire questa riga di comando con privilegi di amministratore:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> La \\ cartella SxS di origine non deve essere utilizzata come meccanismo di ridistribuzione poiché non si tratta di un meccanismo supportato.



## <a name="solution"></a>Soluzione

**Per i consumer:**

Windows 8 include un meccanismo che abilita automaticamente .NET Framework 3,5 quando si tenta di installare il pacchetto ridistribuibile o quando un programma di installazione dell'applicazione che richiede .NET 3,5 richiama il ridistribuibile.

**Per gli sviluppatori di app e gli amministratori IT:**

Gli amministratori IT possono configurare le app .NET 3,5 per l'esecuzione in .NET 3,5 o .NET 4,5 (a seconda degli elementi già installati). Per eseguire un'app gestita in 3,5 o 4,5, è sufficiente aggiungere una sezione nel file di configurazione dell'applicazione. In questo modo si garantisce che se è installato .NET 3,5, l'app verrà eseguita in .NET 3,5; in caso contrario, l'app viene eseguita in .NET 4,5. Di seguito è riportato un esempio della sezione aggiuntiva nel file di configurazione:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Per gli OEM aziendali:**

Per abilitare .NET Framework 3,5 per le compilazioni PAEE e per le applicazioni che non hanno accesso ai Windows Update:

1.  Copiare \\ \\ le origini SxS \\ dall'immagine ISO di compilazione del sistema operativo montata in dotnet35 o in una cartella simile. Ad esempio:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Impostare il chiave:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Per le aziende:**

Per i computer configurati per l'utilizzo di WSUS per la manutenzione, è possibile impostare una voce del registro di sistema per consentire al computer di utilizzare Windows Update per l'abilitazione di .NET 3,5 anziché WSUS (la manutenzione verrà comunque eseguita da WSUS, se si esegue questa operazione).

-   Impostare il chiave:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Questa voce del registro di sistema può essere impostata anche tramite Criteri di gruppo (criterio computer locale-> configurazione computer-> sistema Modelli amministrativi->. Selezionare l'impostazione specificare le impostazioni per l'installazione e il ripristino dei componenti facoltativi.

Se si seleziona Contact Windows Update direttamente per scaricare il contenuto di ripristino anziché Windows Server Update Services (WSUS), qualsiasi tentativo di aggiungere funzionalità di Windows (ad esempio, .NET Framework 3,5) o di ripristinare funzionalità attiverà i download di file da Windows Update. I computer di destinazione richiedono l'accesso a Internet e a WU per questa opzione. Le normali operazioni di manutenzione continuano a usare WSUS se è stato configurato come origine.

**Nota sull'impostazione del percorso di origine locale tramite le voci del registro di sistema**

Gli amministratori IT possono impostare i percorsi di origine locali per i file .NET 3,5 tramite una voce del registro di sistema, in modo che gli utenti possano utilizzare la finestra di dialogo Aggiungi/Rimuovi funzionalità Windows per abilitare le funzionalità con payload mancante senza dover specificare un percorso di origine. Il valore della voce del registro di sistema può essere controllato tramite criteri di gruppo.

Questa voce del registro di sistema è supportata:



<table>
<thead>
<tr class="header">
<th>Voce</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Percorso di origine locale</td>
<td>REG_EXPAND_SZ</td>
<td>Percorsi di origine locali da utilizzare per impostazione predefinita. È possibile specificare più percorsi; devono essere separate da. Le località verranno ricercate nell'ordine in cui sono specificate. <br/> I percorsi di origine locali specificati nella riga di comando DISM hanno la precedenza su quelli specificati in questa voce del registro di sistema. I percorsi delle cartelle possono essere specificati in questa voce del registro di sistema. <br/> È possibile utilizzare WIMs, ma il percorso deve essere nel file WIM. non è necessario montarlo, ad esempio: <br/> <dl> Wim: \\ machine\share\file.wim: 1<br />
</dl> Si noti il 1 alla fine. È necessario specificare l'indice numerico dell'immagine che si desidera utilizzare nel file WIM. <br/> Per un file WIM montato, il percorso di origine deve fare riferimento alla directory di Windows dell'immagine montata, anziché al punto di montaggio, ad esempio:/Source: <mount_point> \Windows anziché/Source: <mount_point> . <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Risorse

<dl>

[Implementazione dei criteri basati sul Registro di sistema](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>