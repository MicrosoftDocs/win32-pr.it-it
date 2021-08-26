---
description: Terminologia usata per descrivere Transactional NTFS (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossario TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e6e296319dc1a9ccd02834fe6144c28d15d61a0fe0c1ec449a07d81f96dbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900651"
---
# <a name="txf-glossary"></a>Glossario TxF

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**Disponibilità**
</dt> <dd>

Disponibilità significa che un gestore delle risorse interromperà le transazioni anche se ciò interrompe la coerenza in modo che il sistema possa continuare a eseguire nuove operazioni. Il gestore delle risorse predefinito forza la disponibilità nel volume di sistema. Ad esempio, se il log delle transazioni è pieno, non è possibile aggiungere nuovo spazio del log delle transazioni e una transazione precedente che verrebbe interrotta richiede il recapito di un risultato da un gestore di risorse superiore per il completamento di una transazione distribuita, il gestore delle risorse non attenderà il gestore delle transazioni superiore e interromperà tale transazione anche se potenzialmente causa un'interruzione della coerenza.

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**Coerenza**
</dt> <dd>

Coerenza significa che un gestore delle risorse avrà esito negativo per le nuove transazioni se non è in grado di procedere in avanti. Ad esempio, se il log delle transazioni è pieno, non è possibile aggiungere nuovo spazio del log delle transazioni e una transazione precedente che verrebbe interrotta richiede che un risultato sia recapitato da un gestore delle risorse superiore per il completamento di una transazione distribuita, il gestore delle risorse attenderà tale risultato.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversione**
</dt> <dd>

Una miniversione è una versione di un file creata da un writer transazionale durante una transazione. La miniversione può essere aperta in un secondo momento nella transazione con accesso in sola lettura.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lettore transazione**
</dt> <dd>

Un lettore transazione è un handle di file transazionato aperto con qualsiasi autorizzazione che fa parte dell'accesso in lettura generico, ma non fa parte dell'accesso in scrittura generico.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**writer transazione**
</dt> <dd>

Un writer transazione è un handle di file transazione aperto con qualsiasi autorizzazione che non fa parte dell'accesso in lettura generico, ma fa parte dell'accesso in scrittura generico.

</dd> </dl>

 

 



