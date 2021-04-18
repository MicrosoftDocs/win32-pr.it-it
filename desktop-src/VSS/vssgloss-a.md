---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307152"
---
# <a name="a-volume-shadow-copy-service"></a>A (Servizio Copia Shadow del volume)

A [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Evento Abort**
</dt> <dd>

Evento VSS emesso dal Servizio Copia Shadow del volume che indica che un'operazione di backup o ripristino conforme è stata interrotta. Il gestore eventi è **CVssWriter:: OnAbort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Il servizio Active Directory (ADSI) è un servizio basato su COM che fornisce un meccanismo per l'individuazione, l'identificazione e l'accesso agli utenti e alle risorse disponibili in un sistema di ambiente di elaborazione distribuita. In particolare, il servizio Active Directory viene utilizzato per gestire le informazioni sulle directory aziendali per la distribuzione da parte di un server di dominio Windows.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mapping del percorso alternativo**
</dt> <dd>

Un percorso diverso dal percorso originale di un file, in cui il file può essere ripristinato in determinate condizioni. In genere, i mapping dei percorsi alternativi non sono definiti per un singolo file ben definito, ma per una coppia di specifiche di percorso/file e possono essere ricorsivi.

Un mapping del percorso alternativo viene usato solo durante un'operazione di ripristino e non deve essere confuso con un percorso alternativo, che viene usato solo durante un'operazione di backup. Vedere anche *percorso alternativo*.

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**percorso alternativo**
</dt> <dd>

Durante le operazioni di backup, una coppia di specifiche di percorso/file (gestita da un'istanza dell'interfaccia **IVssWMFiledesc** ) ha un percorso alternativo se il descrittore del file (come restituito da **IVssWMFiledesc:: GetAlternateLocation**) è diverso da null. Da questo percorso, invece del percorso specificato predefinito, i file devono essere copiati quando viene eseguito il backup di un volume.

Un percorso alternativo viene usato solo durante un'operazione di backup e non deve essere confuso con un mapping del percorso alternativo. Un mapping del percorso alternativo viene usato solo durante le operazioni di ripristino. Vedere anche *mapping del percorso alternativo*.

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**livello applicazione**
</dt> <dd>

Utilizzato da VSS per indicare il punto nel corso della creazione di una copia shadow a cui un writer riceve un blocco. Vedere anche [*applicazioni di livello back-end*](vssgloss-b.md), [*blocco*](vssgloss-f.md), [*applicazioni di livello front-end*](vssgloss-f.md), [*Copia Shadow*](vssgloss-s.md), [*applicazioni a livello di sistema*](vssgloss-s.md), [*writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**copia shadow recuperata automaticamente**
</dt> <dd>

Una copia shadow che ha eseguito un'elaborazione aggiuntiva da parte di un writer è in uno stato completamente coerente per le azioni di backup o data mining (ad esempio, il rollback di tutte le transazioni non ancora completate nel punto in cui è stata creata la copia shadow). Questo può essere avviato da un writer specificando un flag appropriato dall'enumerazione dei **\_ \_ flag del componente VSS** nel membro **dwComponentFlags** della struttura **\_ COMPONENTINFO VSS** o da un richiedente aggiungendo il flag **VSS \_ VolSnap \_ attr \_ rollback \_ Recovery** al contesto per la copia shadow. Il ripristino automatico consente di usare i dati copiati in modalità shadow in un volume di sola lettura, ad data mining, ripristini parziali, ad esempio gli elementi selezionati in un database, o altri scopi.

Vedere anche [*copia shadow trasportabile*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**copia shadow della versione automatica**
</dt> <dd>

Copia shadow che verrà eliminata al termine di un'operazione di backup. A livello di codice, ciò significa che la copia shadow verrà eliminata quando viene rilasciata l'interfaccia **IVssBackupComponents** . Una copia shadow con rilascio automatico non può essere persistente.

Per impostazione predefinita, tutte le copie shadow sono rilasciate automaticamente. Vedere anche [*Copia Shadow persistente*](vssgloss-p.md), [*copia shadow trasportabile*](vssgloss-t.md).

</dd> </dl>

 

 



