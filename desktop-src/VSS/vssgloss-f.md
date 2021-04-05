---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751543"
---
# <a name="f-volume-shadow-copy-service"></a>F (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente del gruppo di file**
</dt> <dd>

Gruppo di file diversi da quelli usati come database e definiti da un writer per la necessità di essere gestiti come unità durante le operazioni di backup e ripristino. Vedere anche [*componente*](vssgloss-c.md), [*componente di database*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**set di file**
</dt> <dd>

Combinazione di un percorso, una specifica del file e un flag ricorsivo che descrive uno di un file o un gruppo di file. Ad esempio, i file vengono aggiunti ai componenti nei set di file.

Se non diversamente specificato, i percorsi di un set di file sono percorsi standard di Windows e possono contenere variabili di ambiente (ad esempio,% SystemRoot%) ma non può contenere caratteri jolly. Non è necessario che il percorso termini con una barra rovesciata (" \\ "). Sono le applicazioni che recuperano queste informazioni per verificarle.

La specifica del file contenuta in un set di file indica il nome del file o dei file inclusi. Questa specifica del file non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata), ma può contenere? e \* caratteri jolly.

Il tag ricorsivo è un valore booleano che specifica se il percorso del set di file deve essere trattato come una sola directory o se indica una gerarchia di directory da attraversare in modo ricorsivo. Il valore booleano è **true** se il percorso viene considerato come una gerarchia di directory da attraversare in modo ricorsivo; in caso contrario, **false** .

Le informazioni su un set di file vengono restituite tramite istanze dell'interfaccia **IVssWMFiledesc** e possono contenere informazioni aggiuntive, tra cui percorsi alternativi, mapping dei percorsi alternativi e impostazioni di supporto dello schema a livello di file.

Vedere anche [*percorso alternativo*](vssgloss-a.md), [*mapping del percorso alternativo*](vssgloss-a.md), [*componente*](vssgloss-c.md), *specifica del file*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Specifica file**
</dt> <dd>

Utilizzato per la corrispondenza dei file all'interno di una directory e per la definizione di un set di file. Non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata), ma può contenere? e \* caratteri jolly.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servizio Replica file**
</dt> <dd>

Utilizzato per replicare i file di sistema in una directory di volume di sistema ridondante (SysVol) per supportare file system la sopravvivenza, in particolare per i file system distribuiti.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**congelare**
</dt> <dd>

Periodo di tempo durante il processo di creazione della copia shadow quando tutti i writer hanno scaricato le scritture nei volumi e non stanno avviando scritture aggiuntive.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Blocca evento**
</dt> <dd>

Evento VSS che indica che è in corso un blocco della copia shadow. Vedere anche *Freeze*, [*Copia Shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**applicazioni di livello front-end**
</dt> <dd>

Indica il punto al quale un writer riceve una notifica di blocco da parte del servizio Copia Shadow del volume. I writer inizializzati come applicazioni di livello front-end ricevono una notifica prima che i writer siano inizializzati come applicazioni di livello back-end o come applicazioni a livello di sistema. Vedere anche il [*livello applicazione*](vssgloss-a.md), [*le applicazioni a livello di back-end*](vssgloss-b.md), [*le applicazioni a livello di sistema*](vssgloss-s.md)e il [*writer*](vssgloss-w.md).

</dd> </dl>

 

 



