---
title: .NET Framework impostazioni predefinite
description: .NET Framework 4.5 è l'impostazione predefinita e .NET Framework 3.5 è facoltativa
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b45aef294e035f5fb7e647c49b22206ac8aadd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883127"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4.5 è l'impostazione predefinita e .NET Framework 3.5 è facoltativa

## <a name="platforms"></a>Piattaforme

**Client** Windows 8     
**Server** Windows Server 2012     

## <a name="description"></a>Descrizione

.NET Framework 4.5 è abilitato per impostazione predefinita in Windows 8. Windows 8 non include .NET 3.5 per impostazione predefinita, ma i file per .NET 3.5 sono disponibili nel supporto di installazione di Windows 8 come funzionalità facoltativa.

Se l'utente esegue l'aggiornamento da Windows 7 a Windows 8, .NET Framework 3.5 è completamente abilitato per garantire che tutte le app nel computer continuino a funzionare correttamente.

## <a name="manifestation"></a>Manifestazione

Se l'utente esegue un'installazione pulita di Windows 8 e quindi installa le app che richiedono .NET Framework 3.5 (o 2.0), attiverà una richiesta per i file .NET 3.5 necessari. In genere i file mancanti verranno scaricati da Windows Update (dopo aver chiesto l'autorizzazione all'utente), ma se l'accesso a Windows Update non è possibile, l'abilitazione di .NET Framework 3.5 avrà esito negativo a meno che non sia stata specificata un'origine alternativa per i file mancanti.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per abilitare .NET Framework 3.5 solo in computer di test con installazioni pulite di Windows 8:

1.  Copiare i file SX di origine dall'immagine ISO di compilazione del sistema \\ \\ operativo \\ montata in dotnet35 o in una cartella simile. Ad esempio:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Eseguire questa riga di comando con privilegi di amministratore:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> La cartella \\ SxS di origine non deve essere usata come meccanismo di ridistribuzione perché non è un meccanismo supportato.



## <a name="solution"></a>Soluzione

**Per i consumer:**

Windows 8 include un meccanismo che abilita automaticamente .NET Framework 3.5 quando si tenta di installare il pacchetto ridistribuibile o quando un programma di installazione di applicazioni che richiede .NET 3.5 richiama il ridistribuibile.

**Per gli sviluppatori di app (e gli amministratori IT):**

Gli amministratori IT possono configurare le app .NET 3.5 per l'esecuzione in .NET 3.5 o .NET 4.5 (a seconda di ciò che è già installato). Per eseguire un'app gestita nella versione 3.5 o 4.5, è sufficiente aggiungere una sezione nel file di configurazione dell'applicazione. In questo modo, se è installato .NET 3.5, l'app verrà eseguita in .NET 3.5. In caso contrario, l'app verrà eseguita in .NET 4.5. Di seguito è riportato un esempio della sezione aggiuntiva nel file di configurazione:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Per gli OEM aziendali:**

Per abilitare .NET Framework 3.5 per le build EEAP e per le applicazioni che non hanno accesso a Windows Update:

1.  Copiare \\ i \\ file SX di origine dall'immagine ISO di compilazione del sistema operativo \\ montata nella cartella dotnet35 o simile. Ad esempio:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Impostare regkey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Per le aziende:**

Per i computer configurati per l'uso di WSUS per la manutenzione, è possibile impostare una voce del Registro di sistema per consentire al computer di usare Windows Update per l'abilitazione di .NET 3.5 invece di WSUS. In questo caso, la manutenzione verrà comunque eseguita da WSUS.

-   Impostare regkey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Questa voce del Registro di sistema può essere impostata anche tramite Criteri di gruppo (Criteri del computer locale -> Configurazione computer -> Modelli amministrativi -> sistema. Selezionare l'impostazione Specificare le impostazioni per l'installazione e il ripristino dei componenti facoltativi.

Se si seleziona Contatta Windows Update direttamente per scaricare il contenuto di ripristino anziché Windows Server Update Services (WSUS), qualsiasi tentativo di aggiungere funzionalità di Windows (ad esempio, .NET Framework 3.5) o funzionalità di ripristino attiverà i download di file da Windows Update. I computer di destinazione richiedono l'accesso a Internet e WU per questa opzione. Le normali operazioni di manutenzione continuano a usare WSUS se è stato configurato come origine.

**Nota relativa all'impostazione del percorso di origine locale tramite le voci del Registro di sistema**

Gli amministratori IT possono impostare percorsi di origine locali per i file .NET 3.5 tramite una voce del Registro di sistema, in modo che gli utenti possano usare la finestra di dialogo Aggiungi/Rimuovi funzionalità di Windows per abilitare le funzionalità con payload mancante senza dover specificare un percorso di origine. Il valore della voce del Registro di sistema può essere controllato tramite Criteri di gruppo.

Questa voce del Registro di sistema è supportata:



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
<td>Percorsi di origine locali da usare per impostazione predefinita. È possibile specificare più percorsi. devono essere separati da ; . Le posizioni verranno ricercate nell'ordine in cui sono specificate. <br/> I percorsi di origine locali specificati nella riga di comando di Gestione e manutenzione immagini distribuzione hanno la precedenza sui percorsi specificati in questa voce del Registro di sistema. I percorsi delle cartelle possono essere specificati in questa voce del Registro di sistema. <br/> È possibile usare wim, ma il percorso deve essere il file WIM. non è necessario montarlo, ad esempio: <br/> <dl> wim: \\ machine\share\file.wim:1<br />
</dl> Si noti il valore 1 alla fine. È necessario specificare l'indice numerico dell'immagine da usare nel file WIM. <br/> Per un file WIM montato, il percorso di origine deve fare riferimento alla directory windows dell'immagine montata, anziché al punto di montaggio (ad esempio: /source: &lt; mount_point &gt; \windows anziché /source: &lt; mount_point &gt; ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Risorse

<dl>

[Implementazione di criteri basati sul Registro di sistema](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>
