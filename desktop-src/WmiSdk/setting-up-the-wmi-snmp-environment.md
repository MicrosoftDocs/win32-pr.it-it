---
description: La comunicazione con un dispositivo di rete tramite l'interfaccia SNMP WMI richiede la configurazione del dispositivo, SNMP e dei servizi WMI. Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurazione dell'ambiente WMI SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349226"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configurazione dell'ambiente WMI SNMP

La comunicazione con un dispositivo di rete tramite l'interfaccia SNMP WMI richiede la configurazione del dispositivo, SNMP e dei servizi WMI. Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.

Le sezioni seguenti sono illustrate in questo argomento:

## <a name="installing-the-snmp-provider"></a>Installazione del provider SNMP

Il servizio SNMP non è abilitato per impostazione predefinita. È possibile abilitare il servizio SNMP e il provider SNMP WMI tramite il pannello di controllo. Tenere presente che il servizio SNMP deve essere abilitato e in esecuzione affinché il provider SNMP WMI funzioni correttamente.

A partire da Windows Vista, utilizzare la procedura seguente per installare il provider SNMP.

**Per installare il provider SNMP**

1.  Dal **Pannello di controllo**, selezionare **programmi**.
2.  In **programmi e funzionalità** fare clic **su attivazione o disattivazione delle funzionalità Windows**.
3.  Nell'elenco funzionalità Windows scorrere fino alla **funzionalità SNMP** ed espandere l'elenco in modo che sia possibile visualizzare il **provider SNMP WMI**.
4.  Selezionare la casella di controllo **provider SNMP WMI**. La casella di controllo per la **funzionalità SNMP** viene selezionata automaticamente perché il provider richiede SNMP.
5.  Fare clic su **OK**.
6.  Da un prompt dei comandi o dal menu **Start** , eseguire Services. msc e verificare che il servizio SNMP sia stato avviato.

## <a name="creating-an-snmp-namespace"></a>Creazione di uno spazio dei nomi SNMP

Uno spazio dei nomi SNMP definisce una visualizzazione di un dispositivo di rete.

> [!Note]  
> Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

 

Nella procedura riportata di seguito viene descritto come creare uno [*spazio dei nomi*](gloss-n.md)WMI SNMP.

**Per creare uno spazio dei nomi SNMP**

1.  Creare un'istanza della classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) compilando un file [*Managed Object Format*](gloss-m.md) . mof o utilizzando l' [API com per WMI](com-api-for-wmi.md).

    Per ulteriori informazioni, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).

2.  Associare i [*qualificatori*](gloss-q.md) del provider SNMP alla definizione dello spazio dei nomi.

    I qualificatori del provider SNMP contengono informazioni sul contesto specifiche dell'implementazione e proprietà del trasporto che definiscono il modo in cui il provider SNMP accede a un dispositivo SNMP. Per ulteriori informazioni, vedere [**qualificatori specifici del provider SNMP**](qualifiers-specific-to-the-snmp-provider.md).

3.  Utilizzare lo strumento da riga di comando [mofcomp](mofcomp.md) per caricare il codice MOF nel repository WMI.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Nell'esempio di codice MOF seguente viene definito lo \\ spazio dei nomi SNMP con un subset dei qualificatori che possono essere associati a uno spazio dei nomi SNMP.

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a>Inserimento di dati MIB SNMP in WMI

Come provider, il provider SNMP funge da Bridge tra i dati SNMP e le classi WMI. Pertanto, è necessario disporre di classi in WMI che rappresentano aspetti diversi di un dispositivo abilitato SNMP. A tale scopo, è necessario utilizzare il compilatore[smi2smir](smi2smir.md)(SNMP Information Module) per compilare le informazioni di gestione SNMP dal formato SNMP nelle definizioni dello schema CIM equivalenti. È quindi possibile indirizzare l'output del compilatore di informazioni in un database dello schema SNMP denominato "SNMP Module Information Repository (archivio SMIR)" o a diversi tipi di file MOF.

Il compilatore viene eseguito nella modalità da riga di comando, usando un file MIB come input. Il comando seguente carica il file MIB specificato in archivio SMIR.

**smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configurazione di community SNMP

Come misura di sicurezza, la community SNMP "public" non viene creata per impostazione predefinita. È possibile creare la community come descritto in [impostazioni del registro di sistema](/previous-versions/windows/embedded/ms907028(v=msdn.10))per le community. Se non si dispone di community, creare la community "public" per accedere al provider SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Generazione di file MOF da file MIB

I comandi seguenti sono un esempio di come generare file MOF dai file MIB installati durante l'installazione del provider SNMP.

**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*

**Smi2smir/g** *.. \\ . \\ hostmib. MIB* **>** *hostmib. mof*

**Smi2smir/g** *.. \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*

**Smi2smir/g** *.. \\ . \\ nipx. MIB* **>** *nipx. mof*

**Smi2smir/g** *.. \\ . \\ MIB \_ II. MIB* MIB **>** *\_ II. mof*

**Smi2smir/g** *.. \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*

**Smi2smir/g** *.. \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*

**Smi2smir/g** *.. \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*

**Smi2smir/g** *.. \\ . \\ wfospf. MIB* **>** *wfospf. mof*

**Smi2smir/g** *.. \\ . \\ DHCP. MIB.. \\ . \\ MSFT. MIB* **>** *DHCP. mof*

**Smi2smir/g** *.. \\ . \\ WINS. MIB.. \\ . \\ MSFT. MIB* **>** *WINS. mof*

**Smi2smir/g** *.. \\ . \\ mipx. MIB.. \\ . \\ MSFT. MIB* **>** *mipx. mof*

**Smi2smir/g** *.. \\ . \\ mripsap. MIB.. \\ . \\ MSFT. MIB* **>** *mripsap. mof*

**Smi2smir/g** *.. \\ . \\ msipbtp. MIB.. \\ . \\ MSFT. MIB* **>** *msipbtp. mof*

**Smi2smir/g** *.. \\ . \\ msiprip2. MIB.. \\ . \\ MSFT. MIB* **>** *msiprip2. mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Aggiunta di file MOF SNMP al repository WMI

I comandi seguenti sono un esempio di come aggiungere i file MOF generati dai file MIB al repository WMI. Se si desidera aggiungere i file MOF all'elenco di file da ripristinare automaticamente in un ripristino del [*repository WMI*](gloss-w.md) , aggiungere il flag **-autocover** alla fine di ogni comando. Per ulteriori informazioni su WMI Mofcomp.exe strumento da riga di comando, vedere [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib. mof*

**mofcomp** *ipforwd. mof*

**mofcomp** *nipx. mof*

**mofcomp** *MIB \_ II. mof*

**mofcomp** *lmmib2. mof*

**mofcomp** *mcastmib. mof*

**mofcomp** *rfc2571. mof*

**mofcomp** *wfospf. mof*

**mofcomp** *DHCP. mof*

**mofcomp** *mipx. mof*

**mofcomp** *mripsap. mof*

**mofcomp** *msipbtp. mof*

**mofcomp** *msiprip2. mof*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai dispositivi SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
