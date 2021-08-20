---
description: Uso di VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Uso di VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6406e938a8fb49314511047bb038ec94a5af9151f5c077ad1fb14984e74474f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125867"
---
# <a name="using-vds"></a>Uso di VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

VDS fornisce un'interfaccia per lo sviluppo di script e GUI in grado di semplificare le attività eseguite da un amministratore del server Windows che gestisce un set eterogeneo di sistemi di archiviazione, eseguendo la migrazione dei dati tra diverse configurazioni hardware nel tempo. Se non si ha familiarità con gli oggetti usati nello sviluppo di VDS, vedere il modello a oggetti [VDS](vds-object-model.md).

Alcuni punti prima di iniziare:

-   Anche se VDS include un provider di software, è necessario acquistare separatamente un provider di hardware e l'hardware associato per sfruttare le operazioni del provider di hardware. Per istruzioni sull'installazione, vedere la documentazione fornita dal produttore dell'hardware.
-   Alcune operazioni richiedono volumi formattati con NTFS. Ad esempio, quando si monta un volume in una directory esistente, il volume che contiene la directory deve essere formattato con NTFS. Altri file system non supportano questa operazione. Per informazioni sulle operazioni che richiedono NTFS, vedere la pagina di ogni metodo in VDS Reference (Informazioni [di riferimento su VDS).](vds-reference.md)

## <a name="programming-languages"></a>Linguaggi di programmazione

Usare qualsiasi linguaggio di programmazione adatto per lo sviluppo con COM, ad esempio il linguaggio C o C++.

## <a name="security"></a>Sicurezza

Windows Il firewall è abilitato per impostazione predefinita. Ciò può causare l'esito negativo dell'autenticazione per le interfacce di callback, ad esempio [**IVdsAdviseSink,**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)che possono essere eseguite in modalità remota. Se Windows firewall è abilitato nel client o nel server, è necessario  aggiungere Gestione volumi remoti alla scheda Eccezioni in Windows Firewall.

**Windows Server 2003:** In Windows Server 2003 con Service Pack 2 (SP2) e Windows Server 2003 con Service Pack 1 (SP1), se il firewall Windows è abilitato nel client o nel server  e se il server è configurato per l'uso dell'autenticazione NTLM, è necessario aggiungere le impostazioni seguenti alla scheda Eccezioni in Firewall Windows per il computer appropriato.

| Computer                 | Impostazioni delle eccezioni                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Computer client (locale)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Computer server (remoto) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Si noti Windows firewall non è abilitato per impostazione predefinita fino Windows Server 2003 con SP1.

Un'applicazione che usa VDS deve essere eseguita con l'account di gruppo Backup Operator o Administrators. Senza il privilegio appropriato, un'applicazione può creare un oggetto caricatore del servizio, ma l'oggetto non carica VDS. Restituisce invece un errore che indica che l'accesso a VDS è negato.

Se la rete usa l'autenticazione NTLM, il computer client deve consentire l'accesso anonimo. In questo caso, se il computer client esegue un sistema operativo Windows Server, l'accesso anonimo è abilitato per impostazione predefinita. Se esegue un sistema operativo Windows Client, l'accesso anonimo deve essere abilitato usando Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Operazioni di configurazione e query

L'ambito delle operazioni di configurazione e query è il computer, il provider, il sottosistema o il pacchetto più pertinenti. Le query attraversano solo un provider o un livello della gerarchia di associazione. Per compilare una visualizzazione completa, il chiamante deve eseguire query su ogni livello. L'elenco seguente include esempi:

-   Per visualizzare tutti i dischi in un computer, i chiamanti devono eseguire query su tutti i provider di software per i dischi che vengono rivendicati da tali provider.
-   Per determinare quali dischi contribuiscono a un volume in pila software, i chiamanti determinano prima i plex che contribuiscono e quindi e infine esercitino una query per gli extent del disco per ogni plex.
-   Per visualizzare tutte le unità collegate a un determinato sottosistema, i chiamanti devono eseguire query sul sottosistema.
-   Per visualizzare tutti i LUN esposti da un sottosistema specificato, i chiamanti devono eseguire query sul sottosistema.
-   Per visualizzare tutte le risorse di archiviazione in una san o in un cluster, i chiamanti devono eseguire query su ogni computer per tutti i provider hardware, eseguire query su ogni provider per tutti i sottosistemi e quindi eseguire query su ogni sottosistema.

Sebbene ogni singola query non restituirà duplicati, le query ripetute tra computer o tra provider possono accumulare duplicati. I chiamanti devono implementare qualsiasi filtro. Si noti anche che le applicazioni di gestione SAN possono usare Active Directory o un repository per rendere persistenti le informazioni di configurazione. potrebbe non essere necessario eseguire query su ogni computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Informazioni di riferimento su VDS](vds-reference.md)
</dt> </dl>

 

