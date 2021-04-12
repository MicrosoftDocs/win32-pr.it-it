---
description: Uso di VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Uso di VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233678"
---
# <a name="using-vds"></a>Uso di VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fornisce un'interfaccia per lo sviluppo di script e GUI in grado di semplificare le attività eseguite da un amministratore di Windows Server che gestisce un set eterogeneo di sistemi di archiviazione, eseguendo la migrazione dei dati tra diverse configurazioni hardware nel tempo. Se non si ha familiarità con gli oggetti usati nello sviluppo VDS, vedere il [modello a oggetti VDS](vds-object-model.md).

Pochi punti prima di iniziare:

-   Sebbene VDS includa un provider di software, è necessario acquistare un provider hardware e l'hardware associato separatamente per sfruttare i vantaggi delle operazioni del provider hardware. Per le istruzioni di installazione, vedere la documentazione fornita dal produttore dell'hardware.
-   Alcune operazioni richiedono volumi formattati in NTFS. Ad esempio, quando si monta un volume in una directory esistente, il volume che contiene la directory deve essere formattato con NTFS. Questa operazione non è supportata dagli altri file System. Per informazioni sulle operazioni che richiedono NTFS, vedere la pagina relativa a ogni metodo in [riferimento a VDS](vds-reference.md).

## <a name="programming-languages"></a>Linguaggi di programmazione

Usare qualsiasi linguaggio di programmazione adatto per lo sviluppo con COM, ad esempio il linguaggio C o C++.

## <a name="security"></a>Sicurezza

Windows Firewall è abilitato per impostazione predefinita. Questo può causare l'esito negativo dell'autenticazione per le interfacce di callback, ad esempio [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), che possono essere eseguite in modalità remota. Se Windows Firewall è abilitato nel client o nel server, è necessario aggiungere Remote Volume Management alla scheda **Exceptions** in Windows Firewall.

**Windows Server 2003:** In Windows Server 2003 con Service Pack 2 (SP2) e Windows Server 2003 con Service Pack 1 (SP1), se Windows Firewall è abilitato nel client o nel server e se il server è configurato per l'utilizzo dell'autenticazione NTLM, è necessario aggiungere le impostazioni seguenti alla scheda **eccezioni** Windows Firewall per il computer appropriato.

| Computer                 | Impostazioni eccezioni                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Computer client (locale)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Computer server (remoto) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Si noti che Windows Firewall non è abilitato per impostazione predefinita fino a Windows Server 2003 con SP1.

Un'applicazione che usa VDS deve essere eseguita con l'account di gruppo Backup Operator o Administrators. Senza il privilegio appropriato, un'applicazione può creare un oggetto caricatore del servizio, ma l'oggetto non caricherà la funzione VDS. Viene invece restituito un errore che indica che l'accesso a VDS è stato negato.

Se la rete usa l'autenticazione NTLM, il computer client deve consentire l'accesso anonimo. In questo caso, se nel computer client è in esecuzione un sistema operativo Windows Server, l'accesso anonimo è abilitato per impostazione predefinita. Se è in esecuzione un sistema operativo client Windows, è necessario abilitare l'accesso anonimo usando Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Operazioni di configurazione e query

Le operazioni di configurazione e query sono limitate dall'ambito del computer, del provider, del sottosistema o del pacchetto più rilevante. Le query attraversano solo un provider o un livello della gerarchia di binding. Per compilare una visualizzazione completa, il chiamante deve eseguire una query su tutti i livelli. Nell'elenco seguente sono inclusi alcuni esempi:

-   Per visualizzare tutti i dischi in un computer, i chiamanti devono eseguire una query su tutti i provider di software per i dischi richiesti da tali provider.
-   Per determinare quali dischi contribuiscono a un volume in pila software, i chiamanti determinano innanzitutto i plex che contribuiscono e quindi eseguono una query per gli extent del disco per ogni plex.
-   Per visualizzare tutte le unità collegate a un determinato sottosistema, i chiamanti devono eseguire una query sul sottosistema.
-   Per visualizzare tutti i LUN esposti da un determinato sottosistema, i chiamanti devono eseguire una query sul sottosistema.
-   Per visualizzare tutte le risorse di archiviazione in una rete SAN o un cluster, i chiamanti devono eseguire una query su ogni computer per tutti i provider hardware, eseguire una query su ogni provider per tutti i sottosistemi, quindi eseguire una query su ogni sottosistema.

Mentre ogni singola query non restituirà duplicati, le query ripetute tra più computer o tra i provider possono accumulare duplicati. I chiamanti devono implementare qualsiasi filtro. Si noti inoltre che le applicazioni di gestione SAN possono utilizzare il Active Directory o un repository per salvare in modo permanente le informazioni di configurazione; potrebbe non essere necessario eseguire una query su ogni computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Riferimento VDS](vds-reference.md)
</dt> </dl>

 

