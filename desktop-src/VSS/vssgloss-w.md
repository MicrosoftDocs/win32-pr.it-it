---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526268"
---
# <a name="w-volume-shadow-copy-service"></a>W (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protezione file di Windows**
</dt> <dd>

Servizio di sistema che protegge i file speciali del sistema operativo. Se uno di questi file viene eliminato o sovrascritto, la protezione dei file di Windows sostituisce il file con quello originale dalla relativa cache.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Writer**
</dt> <dd>

Applicazione che coordina le operazioni di I/O con la copia shadow VSS e le operazioni correlate alla copia shadow, ad esempio backup e ripristini, in modo che i dati contenuti nel volume copiato Shadow siano in uno stato coerente.

Per supportare questo coordinamento, un writer deve implementare un'istanza di una classe derivata dalla classe di base astratta **CVssWriter** per comunicare con l'infrastruttura VSS. Vedere anche [*Copia Shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe Writer**
</dt> <dd>

Identificatore univoco globale (GUID) fornito da un writer durante l'inizializzazione per indicare che appartiene a un tipo specificato di writer. Ad esempio, più implementazioni di un writer possono condividere lo stesso ID di classe Writer.

I writer della stessa classe possono essere distinti dalle istanze del writer. È spetta a uno sviluppatore di applicazioni specificare le classi writer. Vedere anche *istanza del writer*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**istanza writer**
</dt> <dd>

Identificatore univoco globale (GUID) fornito da VSS per ogni processo del writer eseguito in un sistema. Ogni volta che viene avviato il writer, viene generato un valore univoco per l'istanza del writer.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento di metadati del writer**
</dt> <dd>

Documento XML creato da un writer (usando l'interfaccia **IVssCreateWriterMetadata** ) che contiene informazioni sullo stato e sui componenti del writer. Un richiedente può eseguire query sui documenti di metadati del writer (usando l'interfaccia **IVssExamineWriterMetadata** ) quando si esegue un'operazione di ripristino o di backup.

Un documento di metadati del writer contiene l'elenco di tutti i componenti di un writer, ciascuno dei quali può partecipare a un backup. Questo comportamento è diverso dal documento relativo ai componenti di backup del richiedente, che contiene solo i componenti inclusi in modo esplicito per un'operazione di backup o ripristino.

Una volta creato, il documento di metadati del writer deve essere visualizzato come oggetto di sola lettura. Può essere salvato su disco. Vedere anche [*documento sui componenti di backup*](vssgloss-b.md), [*inclusione di componenti espliciti*](vssgloss-e.md), [*inclusione di componenti impliciti*](vssgloss-i.md).

</dd> </dl>

 

 



