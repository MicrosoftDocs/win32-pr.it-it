---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56eef69a16a77fce7f557ae0ff02ff0e5d84d0225d082fd486af629b9804aeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056199"
---
# <a name="f-volume-shadow-copy-service"></a>F (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente del gruppo di file**
</dt> <dd>

Gruppo di file diversi da quelli usati come database e definiti da un writer che devono essere gestiti come unità durante le operazioni di backup e ripristino. Vedere anche [*componente*](vssgloss-c.md), [*componente di database*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**set di file**
</dt> <dd>

Combinazione di un percorso, una specifica di file e un flag ricorsivo che descrive uno di un file o un gruppo di file. Ad esempio, i file vengono aggiunti ai componenti nei set di file.

Se non diversamente indicato, i percorsi di un set di file sono percorsi Windows standard e possono contenere variabili di ambiente ,ad esempio %SystemRoot%), ma non possono contenere caratteri jolly. Non è necessario che il percorso termina con una barra rovesciata (" \\ "). Sono le applicazioni che recuperano queste informazioni a verificarlo.

La specifica di file contenuta in un set di file indica il nome del file o dei file inclusi. Questa specifica di file non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata) ma può contenere ? e \* caratteri jolly.

Il tag ricorsivo è un valore booleano che specifica se il percorso del set di file deve essere considerato come una sola directory o se indica una gerarchia di directory da attraversare in modo ricorsivo. Il valore **booleano è true** se il percorso viene considerato come una gerarchia di directory da attraversare in modo ricorsivo oppure **false** in caso contrario.

Le informazioni su un set di file vengono restituite tramite istanze dell'interfaccia **IVssWMFiledesc** e possono contenere informazioni aggiuntive che includono percorsi alternativi, mapping di percorsi alternativi e impostazioni di supporto dello schema a livello di file.

Vedere anche [*percorso alternativo*](vssgloss-a.md), mapping [*percorso alternativo*](vssgloss-a.md), [*componente*](vssgloss-c.md), specifica *del file*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**specifica del file**
</dt> <dd>

Usato per trovare la corrispondenza con i file all'interno di una directory e per definire un set di file. Non può contenere specifiche di directory (ad esempio, nessuna barra rovesciata), ma può contenere ? e \* caratteri jolly.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servizio Replica file**
</dt> <dd>

Usato per replicare i file di sistema in una directory del volume di sistema ridondante (SysVol) per supportare file system sopravvivenza, in particolare per i file system distribuiti.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Congelare**
</dt> <dd>

Periodo di tempo durante il processo di creazione della copia shadow quando tutti i writer hanno scaricato le scritture nei volumi e non avviano scritture aggiuntive.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Evento Freeze**
</dt> <dd>

Evento VSS che indica che è in corso un blocco della copia shadow. Vedere anche *bloccare*, [*copia shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**applicazioni di livello front-end**
</dt> <dd>

Indica il punto in cui un writer viene informato di un blocco da parte di VSS. I writer inizializzati come applicazioni di livello front-end vengono informati prima dei writer inizializzati come applicazioni di livello back-end o come applicazioni a livello di sistema. Vedere anche applicazioni a [*livello di*](vssgloss-a.md)applicazione, [*applicazioni back-end,*](vssgloss-b.md) [*applicazioni a livello di sistema,*](vssgloss-s.md) [*writer.*](vssgloss-w.md)

</dd> </dl>

 

 



