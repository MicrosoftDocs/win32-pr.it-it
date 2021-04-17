---
description: Glossario dei termini usati nella documentazione di Windows Virtualization SDK.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glossario di Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233314"
---
# <a name="hyper-v-glossary"></a>Glossario di Hyper-V

In questo argomento viene fornito un glossario dei termini utilizzati nella documentazione di Windows Virtualization SDK.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**associazione**
</dt> <dd>

Processo mediante il quale i servizi e i livelli software sono collegati tra loro. Quando viene installato un servizio di rete, vengono stabilite le relazioni di associazione e le dipendenze per i servizi.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Checkpoint**
</dt> <dd>

Uno snapshot di una macchina virtuale che consente a un amministratore di ripristinare lo stato della macchina virtuale al momento della creazione del checkpoint.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**Compact**
</dt> <dd>

Per ridurre le dimensioni di un disco rigido virtuale a espansione dinamica, rimuovendo lo spazio inutilizzato dal file con estensione vhd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco rigido virtuale differenze**
</dt> <dd>

Disco rigido virtuale in cui sono archiviate le modifiche apportate a un disco rigido virtuale padre associato allo scopo di mantenere intatto il padre. Il disco differenze è un file con estensione vhd separato associato al file con estensione vhd del disco padre. Le modifiche continuano ad accumularsi nel disco differenze fino a quando non vengono unite al disco padre.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco rigido virtuale a espansione dinamica**
</dt> <dd>

Disco rigido virtuale che aumenta di dimensioni ogni volta che viene modificato. Questo tipo di disco rigido virtuale inizia come file con estensione VHD da 3 KB e può aumentare fino a raggiungere le dimensioni massime specificate al momento della creazione del file. L'unico modo per ridurre le dimensioni del file consiste nello azzerare i dati eliminati, quindi compattare il disco rigido virtuale.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco rigido virtuale a dimensione fissa**
</dt> <dd>

Un disco rigido virtuale con una dimensione fissa determinata e per cui tutto lo spazio viene allocato quando viene creato il disco. Le dimensioni del disco non cambiano quando i dati vengono aggiunti o eliminati.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Macchina virtuale di prima generazione**
</dt> <dd>

Una macchina virtuale (VM) che contiene lo stesso hardware virtuale presente nelle versioni di Hyper-V precedenti a Windows 8.1 e Windows Server 2012 R2

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Macchina virtuale di seconda generazione**
</dt> <dd>

Una macchina virtuale (VM) che contiene un modello di hardware virtuale semplificato e usa il firmware UEFI anziché il BIOS. In questa VM la maggior parte dei dispositivi emulati viene rimossa, riducendo la complessità della gestione e la superficie di attacco alla sicurezza.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operativo guest**
</dt> <dd>

Il sistema operativo installato nella macchina virtuale.

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Integration Services**
</dt> <dd>

Una raccolta di servizi e driver software che massimizzano le prestazioni e offrono un'esperienza utente migliore all'interno di una macchina virtuale. I servizi di integrazione sono disponibili solo per i sistemi operativi guest supportati.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**coppia chiave-valore**
</dt> <dd>

Set di elementi di dati che contiene un identificatore univoco, denominato chiave, e un valore che rappresenta i dati effettivi della chiave.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**computer fisico**
</dt> <dd>

Un computer basato su hardware, anziché una macchina virtuale basata su software.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**stato salvato**
</dt> <dd>

Modalità di archiviazione di una macchina virtuale in modo che possa essere ripresa rapidamente, in modo analogo a un computer portatile in stato di ibernazione. Quando si inserisce una macchina virtuale in esecuzione in uno stato salvato, Virtual Server e Hyper-V arrestano la macchina virtuale, scrivono i dati presenti in memoria in file temporanei e interrompono il consumo delle risorse di sistema. Il ripristino di una macchina virtuale da uno stato salvato restituisce la stessa condizione in cui si trovava al momento del salvataggio dello stato.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disco floppy virtuale**
</dt> <dd>

Una versione basata su file di un disco floppy fisico. Un disco floppy virtuale viene archiviato come file con estensione vfd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco rigido virtuale**
</dt> <dd>

Supporto di archiviazione per una macchina virtuale. Può risiedere in qualsiasi topologia di archiviazione accessibile dal sistema operativo host, tra cui dispositivi esterni, reti dell'area di archiviazione e archiviazione collegata alla rete. L'estensione del nome file è VHD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**macchina virtuale**
</dt> <dd>

Un computer all'interno di un computer, implementato nel software. Una macchina virtuale emula un sistema hardware completo, dal processore alla scheda di rete, in un ambiente software autosufficiente e isolato, consentendo il funzionamento simultaneo di sistemi operativi altrimenti incompatibili. Ogni sistema operativo figlio viene eseguito in una macchina virtuale software isolata.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configurazione macchina virtuale**
</dt> <dd>

Configurazione delle risorse assegnate a una macchina virtuale. Gli esempi includono dispositivi come dischi e schede di rete, nonché memoria e processori.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Servizio Virtual Machine Management**
</dt> <dd>

Servizio Hyper-V che consente di gestire l'accesso alle macchine virtuali.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**snapshot macchina virtuale**
</dt> <dd>

Snapshot basato su file dello stato, dei dati del disco e della configurazione di una macchina virtuale in un momento specifico.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**rete virtuale**
</dt> <dd>

Versione virtuale di uno switch di rete fisica. Una rete virtuale può essere configurata per fornire accesso alle risorse di rete locali o esterne per una o più macchine virtuali.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gestione reti virtuali**
</dt> <dd>

Servizio Hyper-V usato per creare e gestire reti virtuali.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**Commuter virtuale**
</dt> <dd>

Vedere rete virtuale.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Ridimensionamento VHDX**
</dt> <dd>

Operazione che compatta o espande un disco rigido virtuale.

</dd> </dl>

 

 



