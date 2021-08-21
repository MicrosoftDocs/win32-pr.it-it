---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb67a0f4ae622e0fead791d1876236794806c9b9e725d1c60f7712fd44cbe573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842563"
---
# <a name="w-volume-shadow-copy-service"></a>W (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T U](vssgloss-t.md) [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows Protezione file**
</dt> <dd>

Servizio di sistema che protegge file speciali del sistema operativo. Se uno di questi file viene eliminato o sovrascritto, Windows File Protection sostituisce il file con l'originale dalla cache.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Scrittore**
</dt> <dd>

Un'applicazione che coordina le operazioni di I/O con le operazioni correlate alla copia shadow di Vss e alla copia shadow (ad esempio backup e ripristini) in modo che i dati contenuti nel volume shadow copiato siano in uno stato coerente.

Per supportare questo coordinamento, un writer deve implementare un'istanza di una classe derivata dalla classe di base astratta **CVssWriter** per comunicare con l'infrastruttura vss. Vedere anche [*copia shadow.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Classe writer**
</dt> <dd>

Identificatore univoco globale (GUID) fornito da un writer durante l'inizializzazione per indicare che appartiene a un determinato tipo di writer. Ad esempio, più implementazioni di un writer possono condividere lo stesso ID di classe writer.

I writer della stessa classe possono essere distinti dalle relative istanze del writer. Lo sviluppatore di applicazioni deve specificare le classi writer. Vedere anche istanza *del writer*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**Istanza del writer**
</dt> <dd>

Identificatore univoco globale (GUID) fornito da VSS per ogni processo di scrittura in esecuzione in un sistema. Un valore univoco per l'istanza del writer viene generato ogni volta che viene avviato il writer.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento di metadati del writer**
</dt> <dd>

Documento XML creato da un writer (usando **l'interfaccia IVssCreateWriterMetadata)** contenente informazioni sullo stato e sui componenti del writer. Un richiedente può eseguire query sui documenti dei metadati del writer **(usando l'interfaccia IVssExamineWriterMetadata)** quando esegue un'operazione di ripristino o backup.

Un documento di metadati del writer contiene l'elenco di tutti i componenti di un writer, uno dei quali potrebbe partecipare a un backup. Ciò differisce dal documento Componenti di backup del richiedente, che contiene solo i componenti inclusi in modo esplicito per un'operazione di backup o ripristino.

Dopo la costruzione, il documento di metadati del writer deve essere visualizzato come oggetto di sola lettura. Può essere salvato su disco. Vedere anche [*Documento dei componenti di backup*](vssgloss-b.md), inclusione esplicita dei [*componenti,*](vssgloss-e.md) [*inclusione implicita dei componenti*](vssgloss-i.md).

</dd> </dl>

 

 



