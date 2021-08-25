---
description: La comunicazione con un dispositivo di rete tramite l'interfaccia WMI SNMP richiede la configurazione del dispositivo, SNMP e dei servizi WMI. Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurazione dell'ambiente SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a090dab219c589fc8d9084c445e9a69c8d75afefb64400fe3029bfed66ab931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860412"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configurazione dell'ambiente SNMP WMI

La comunicazione con un dispositivo di rete tramite l'interfaccia WMI SNMP richiede la configurazione del dispositivo, SNMP e dei servizi WMI. Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.

In questo argomento vengono illustrate le sezioni seguenti:

## <a name="installing-the-snmp-provider"></a>Installazione del provider SNMP

Il servizio SNMP non è abilitato per impostazione predefinita. È possibile abilitare il servizio SNMP e il provider SNMP WMI tramite il Pannello di controllo. Tenere presente che il servizio SNMP deve essere abilitato e in esecuzione per il funzionamento del provider WMI SNMP.

A partire Windows Vista, usare la procedura seguente per installare il provider SNMP.

**Per installare il provider SNMP**

1.  Nella **Pannello di controllo** selezionare **Programmi.**
2.  In **Programmi e funzionalità** selezionare Attiva Windows funzionalità **di**.
3.  Nell'elenco Windows funzionalità, scorrere verso il basso fino alla funzionalità **SNMP** ed espandere l'elenco in modo da visualizzare **Provider SNMP WMI.**
4.  Selezionare la casella di controllo **per Provider SNMP WMI.** La casella di controllo **per la funzionalità SNMP** viene selezionata automaticamente perché il provider richiede SNMP.
5.  Fare clic su **OK**.
6.  Da un prompt dei comandi o dal menu **Start** eseguire Services.msc e verificare che il servizio SNMP sia avviato.

## <a name="creating-an-snmp-namespace"></a>Creazione di uno spazio dei nomi SNMP

Uno spazio dei nomi SNMP definisce una visualizzazione di un dispositivo di rete.

> [!Note]  
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

Nella procedura seguente viene descritto come creare uno spazio dei nomi [*WMI*](gloss-n.md)SNMP.

**Per creare uno spazio dei nomi SNMP**

1.  Creare un'istanza della classe di sistema [**\_ \_ Namespace**](--namespace.md) compilando un file [*Managed Object Format*](gloss-m.md) con estensione mof o usando l'API [COM per WMI.](com-api-for-wmi.md)

    Per altre informazioni, vedere Creazione [di gerarchie all'interno di WMI.](creating-hierarchies-within-wmi.md)

2.  Associare i qualificatori del provider SNMP [*alla*](gloss-q.md) definizione dello spazio dei nomi.

    I qualificatori del provider SNMP contengono informazioni di contesto specifiche dell'implementazione e proprietà di trasporto che definiscono il modo in cui il provider SNMP accede a un dispositivo SNMP. Per altre informazioni, vedere [**Qualificatori specifici del provider SNMP.**](qualifiers-specific-to-the-snmp-provider.md)

3.  Usare lo strumento da riga di comando [mofcomp](mofcomp.md) per caricare il codice MOF nel repository WMI.

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

L'esempio di codice MOF seguente definisce lo spazio dei nomi snmp con un subset dei qualificatori che possono essere \\ associati a uno spazio dei nomi SNMP.

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

In quanto provider, il provider SNMP funge da ponte tra i dati SNMP e le classi WMI. Pertanto, è necessario disporre di classi in WMI che rappresentano aspetti diversi di un dispositivo abilitato per SNMP. A tale scopo, è necessario usare il compilatore del modulo di informazioni SNMP ([smi2smir](smi2smir.md)) per compilare le informazioni di gestione SNMP dal formato SNMP nelle definizioni dello schema CIM equivalenti. È quindi possibile indirizzare l'output del compilatore di informazioni in un database dello schema SNMP denominato "SNMP Module Information Repository (SMIR)" o in diversi tipi di file MOF.

Il compilatore viene eseguito in modalità riga di comando, usando un file MIB come input. Il comando seguente carica il file MIB specificato in SMIR.

**smi2smir /a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configurazione delle community SNMP

Come misura di sicurezza, la community "pubblica" SNMP non viene creata per impostazione predefinita. È possibile creare la community come descritto in [Community Registry Impostazioni](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Se non si ha alcuna community, creare la community "pubblica" per accedere al provider SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Generazione di file MOF da file MIB

I comandi seguenti sono un esempio di come generare file MOF dai file MIB installati quando viene installato il provider SNMP.

**cd** *%windir% \\ system32 \\ wbem \\ SNMP*

**Smi2smir /g** *.. \\ .. \\ hostmib.mib* **>** *hostmib.mof*

**Smi2smir /g** *.. \\ .. \\ ipforwd.mib* **>** *ipforwd.mof*

**Smi2smir /g** *.. \\ .. \\ nipx.mib* **>** *nipx.mof*

**Smi2smir /g** *.. \\ .. \\ mib \_ ii.mib* **>** *mib \_ ii.mof*

**Smi2smir /g** *.. \\ .. \\ lmmib2.mib* **>** *lmmib2.mof*

**Smi2smir /g** *.. \\ .. \\ mcastmib.mib* **>** *mcastmib.mof*

**Smi2smir /g** *.. \\ .. \\ rfc2571.mib* **>** *rfc2571.mof*

**Smi2smir /g** *.. \\ .. \\ wfospf.mib* **>** *wfospf.mof*

**Smi2smir /g** *.. \\ .. \\ dhcp.mib.. \\ .. \\ msft.mib* **>** *dhcp.mof*

**Smi2smir /g** *.. \\ .. \\ wins.mib.. \\ .. \\ msft.mib* **>** *wins.mof*

**Smi2smir /g** *.. \\ .. \\ mipx.mib.. \\ .. \\ msft.mib* **>** *mipx.mof*

**Smi2smir /g** *.. \\ .. \\ mripsap.mib.. \\ .. \\ msft.mib* **>** *mripsap.mof*

**Smi2smir /g** *.. \\ .. \\ msipbtp.mib.. \\ .. \\ msft.mib* **>** *msipbtp.mof*

**Smi2smir /g** *.. \\ .. \\ msiprip2.mib.. \\ .. \\ msft.mib* **>** *msiprip2.mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Aggiunta di file MOF SNMP al repository WMI

I comandi seguenti sono un esempio di come aggiungere i file MOF generati dai file MIB al repository WMI. Se si desidera aggiungere i file MOF all'elenco di file da ripristinare automaticamente in un ripristino del [*repository WMI,*](gloss-w.md) aggiungere il flag **-AUTORECOVER** alla fine di ogni comando. Per altre informazioni sullo strumento da riga Mofcomp.exe WMI, vedere [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib.mof*

**mofcomp** *ipforwd.mof*

**mofcomp** *nipx.mof*

**mofcomp** *mib \_ ii.mof*

**mofcomp** *lmmib2.mof*

**mofcomp** *mcastmib.mof*

**mofcomp** *rfc2571.mof*

**mofcomp** *wfospf.mof*

**mofcomp** *dhcp.mof*

**mofcomp** *mipx.mof*

**mofcomp** *mripsap.mof*

**mofcomp** *msipbtp.mof*

**mofcomp** *msiprip2.mof*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai dispositivi SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
