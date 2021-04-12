---
description: Terminologia utilizzata per descrivere Transactional NTFS (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossario TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233516"
---
# <a name="txf-glossary"></a>Glossario TxF

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**disponibilità**
</dt> <dd>

La disponibilità indica che un gestore di risorse interrompe le transazioni anche se la coerenza viene interrotta in modo che il sistema possa continuare a eseguire nuove attività. Il gestore di risorse predefinito impone la disponibilità nel volume di sistema. Se, ad esempio, il log delle transazioni è pieno, non è possibile aggiungere nuovi spazi di log delle transazioni e una transazione precedente che verrebbe interrotta richiede il recapito di un risultato da un gestore di risorse superiore per il completamento di una transazione distribuita, il gestore di risorse non attenderà la gestione transazioni superiore e interromperà la transazione, anche se ciò potrebbe interrompere la coerenza.

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**coerenza**
</dt> <dd>

La coerenza indica che un gestore di risorse non riuscirà a eseguire nuove transazioni se non è in grado di avanzare. Se, ad esempio, il log delle transazioni è pieno, non è possibile aggiungere nuovi spazi di log delle transazioni e una transazione meno recente che verrebbe interrotta richiede il recapito di un risultato da un gestore di risorse superiore affinché una transazione distribuita venga completata, il gestore di risorse attenderà tale risultato.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversione**
</dt> <dd>

Un miniversione è una versione di un file creato da un writer transazionale durante una transazione. Miniversione può essere aperto in un secondo momento nella transazione con accesso in sola lettura.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lettore sottoposto a transazione**
</dt> <dd>

Un reader transazionale è un handle di file transazionale aperto con qualsiasi autorizzazione che fa parte di un accesso in lettura generico, ma non fa parte di un accesso in scrittura generico.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Writer transazionale**
</dt> <dd>

Un writer transazionale è un handle di file transazionale aperto con qualsiasi autorizzazione che non fa parte di un accesso in lettura generico, ma fa parte di un accesso in scrittura generico.

</dd> </dl>

 

 



